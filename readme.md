以下のチュートリアルを実施したもの
https://docs.conan.io/2/tutorial/consuming_packages/build_simple_cmake_project.html

# ビルド, 実行までの手順

```
conan profile detect --force
conan install . --output-folder=build --build=missing
cd build
cmake .. -DCMAKE_TOOLCHAIN_FILE=conan_toolchain.cmake -DCMAKE_BUILD_TYPE=Release
cmake --build .
./compressor
```
