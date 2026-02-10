# Yasnen's memo

mkdir ~/keyboards
cd ~/keyboards
git clone https://github.com/Yasnen/keyball.git keyball
git clone https://github.com/qmk/qmk_firmware.git --depth 1 --recurse-submodules --shallow-submodules -b 0.22.14 qmk
cd ~/keyboards/qmk/keyboards
ln -s ../../keyball/qmk_firmware/keyboards/keyball keyball
cd ~/keyboards
make SKIP_GIT=yes keyball/keyball39:yasnen
make clean
