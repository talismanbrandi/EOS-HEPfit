# EOS-HEPfit

#### To install HEPfit:

tar xvzf HEPfit-core-1.0.tar.gz     
mkdir build     
cd build/     
cmake .. -DLOCAL_INSTALL_ALL=ON -DNOMCMC=ON    
make    
make install

#### To make the event generator:

cd examples/EventGeneration   
make

#### To run the event generator:

The configuration files are in the folder called config/BKstll. Copy the folder BKstll to the EventGeneration folder. Then run

./analysis BKstll/StandardModel.conf 0

This will give you the central even corresponding to the central values in the config files

./analysis BKstll/StandardModel.conf 10

will give you the central event and 10 random events

./analysis BKstll/StandardModel.conf 10 SomeFolder

will do the above but instead of printing in the screen will save the parameter values and observables in a folder called GeneratedEvents/SomeFolder.


