# Generate C# code from ONNX proto file

1. Download `onnx-ml.proto3` from https://github.com/onnx/onnx/blob/master/onnx/onnx-ml.proto3
2. Download protobuf C# compiler version 3.0 or greater from 
   https://github.com/google/protobuf/tree/master/csharp
3. Add `option csharp_namespace =
   "Microsoft.ML.UniversalModelFormat.Onnx";` to `onnx-ml.proto3` right below `package ONNX_NAMESPACE;`
4. Assuming the compiler and proto file are saved at
   `E:\protobuf-csharp-port\lib` then run the following in command line to get C# code from the proto file:
   ```
   protoc.exe -I="E:\protobuf-csharp-port\lib" --csharp_out="E:\protobuf-csharp-port\lib" "E:\protobuf-csharp-port\lib\onnx-ml.proto3"
   ```

## The proto3 file is current as of 06/01/2018 and generated from onnx-ml.proto3 based on the following commit https://github.com/onnx/onnx/commit/33e9cd4182fe468675241fba4ae8a16c2f0bd82f