add_library(LLVMObfuscation MODULE
  CryptoUtils.cpp
  Substitution.cpp
  BogusControlFlow.cpp
  Utils.cpp
  SplitBasicBlocks.cpp
  Flattening.cpp
        Entry.cpp)

add_dependencies(LLVMObfuscation intrinsics_gen)
