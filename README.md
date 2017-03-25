# ubuntu14-04_aliceo2
Documentation on the issues of working with ALICE-O2 code in ubuntu 14.04 LTS version
AFTER DOWNLOADING THE SUITABLE "ALICE-O2" package from github (git clone -b mft https://github.com/packagename/AliceO2.git)


cd AliceO2/

mkdir build_o2

cd build_o2/

source /home/debasish/MFT/new_aliceo2/build_fairsoft/FairRoot/bin/FairRootConfig.sh

export FAIRROOTPATH=/home/debasish/MFT/new_aliceo2/build_fairsoft/FairRoot/

cmake -DFAIRROOT_INCLUDE_DIR=$FAIRROOTPATH/include -DFAIRROOT_LIBRARY_DIR=$FAIRROOTPATH/lib -DCMAKE_CXX_FLAGS=-std=c++11 -DBUILD_DOXYGEN=ON -DBOOST_ROOT=/home/debasish/MFT/new_aliceo2/build_fairsoft ..

make

=============if thats 100% OK, then for running macros====================

export ALICE_ROOT=/home/debasish/MFT/new_aliceo2/build_fairsoft/AliRoot/

source /home/debasish/MFT/new_aliceo2/AliceO2/build_o2/config.sh

source /home/debasish/MFT/new_aliceo2/build_fairsoft/DDS/DDS_env.sh


