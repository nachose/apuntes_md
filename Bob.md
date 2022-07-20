## Bob commands

Bob init generate pull --> después de hacer un rebase

Bob build -->compila

Bob image --> genera imágenes docker

Bob test --> corre los tests

Bob test:cpp -->corre solamente tests c++, SFT + UT


### Build data plane in debug

Build data-plane only

./bob/bob init generate

./bob/bob set-artifact-type:debug  → this is to enable debug version. if not, then image will be release

./bob/bob build

./bob/bob set-artifact-type:debug; bob/bob image:prepare; bob/bob image:set-params; bob/bob image:data-plane


## Bob phases

see ruleset2.0.yaml

bob init pull generate build image helm lint bench push




