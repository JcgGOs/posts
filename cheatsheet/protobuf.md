# Protobuf

## Encode/Decode

user.proto
```proto
syntax = "proto3";  //proto2/proto3

package tutorial;   //package name

message City {     //City
  string province = 1;
  double name = 2;
}

message User {     //User
  int64 ID = 1;
  string name = 2;
  repeated City points = 3;
}
```

user.proto.txt
```txt
ID: 12345678
name: "chengdu"
points: [
    {
        province: "SiChuan"
        name: "Chengdu"
    },
    {
        province: "Guangdong"
        name: "Shenzhen"
    }
]
```

### Encode

```shell
# encode to generate a binary
cat user.proto.txt |protoc  --encode tutorial.User user.proto > user.pb
```

### decode
```shell
# decode to a text
protoc --decode tutorial.User user.proto < user.pb

# decode with raw
protoc --decode_raw < user.pb
```