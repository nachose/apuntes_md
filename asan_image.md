## ASAN image

Generate image with asan:</br></br>

env CCACHE_DIR=/workspace/git/${USER}/ccache ./bob/bob -p asan=on init pull generate:3pp

env CCACHE_DIR=/workspace/git/${USER}/ccache ./bob/bob -p asan=on -p cc=clang -p cxx=clang++ generate build

env CCACHE_DIR=/workspace/git/${USER}/ccache ./bob/bob image helm push