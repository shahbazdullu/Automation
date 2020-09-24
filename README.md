Instructions to run the LMChecker
==================================

## Step1:

You can run the LMChecker just in bin directory. Just follow the instructions mentioned below.

1. Go to the bin directory run the following cmd
	./lmchecker.sh --help
_It will guide how you can run the LMChecker_

2. Now run the following cmd  to generate configuration file
	./lmchecker.sh --config
_It will generate a configuration.txt file in the configuration directory, just update it according to your requirements._

3. Update the configuration file according to your requirements.

4. Place all DUT and testbench files in a common directory (DUT files will be different
for all Trainees but Testbench will be same for all )

5. Place expected result file into expected result directory

## Step2:
For dumping the simulation results into a VCD file (optional)
If you want to generate a VCD file, write the following into your testbench file, otherwise, it
will not generate VCD files

```javascript
initial
begin
	$dumpfile("test_XXXX.vcd");
	$dumpvars(0,tb_filename);
end
```
_XXXX are the last four digits of trainees roll no_

**Note:** VCD files will be generated where DUT files are placed

## Step3:
#### This step is only needed when you have a file, whose path is needed to configure into another file.
Update any file in DUT where there is a need to configure the path as in Example directory
you can see the path of ​ "data.bin" ​ is configured into ​ "inst_mm.v"​ file.

## Step4:
Run the LMChecker by running the following command in the terminal
	./lmchecker.sh --run













