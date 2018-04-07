# makeCompD
Makes large number of test files for Steve Mussmann's Comp-D d-statistic program: https://github.com/smussmann82/Comp-D_MPI. Can randomly select individuals, or use provided weights file. 

## Usage
Requires Python3. View the running options by calling the executable using the <-h/--help> flag:
````./makeCompD.py -h

Exiting because help menu was called.

makeCompD.py

Contact:Tyler K. Chafin, University of Arkansas,tkchafin@uark.edu

Usage:  ./makeCompD.py -p </path/to/popmap> -i </path/to/infile> <-s /path/to/stats> <-m int>

Description: Creates input test files for Comp-D (https://github.com/smussmann82/Comp-D_MPI)

	Arguments:
		-p,--popmap	: Path to tab-delimited population map
			-Assumes that all sampled in popmap can be used for CompD tests
		-i,--infile	: Prefix for input file
			Using format of CompD, but with Population IDs from the popmap file
		-w,--weights	: Optional. File containing individual weights
			-Should be formatted as sampleName \t weight
			-Samples with highest weight are chosen. For example, this could be
			 provided as number of loci present. Samples with most loci will be selected
			-Samples missing from weights file will be assigned weights of 0
		-m,--max	: Maximum individuals to sample per populations <default=10>
			-If used without <-s>, samples will be randomly chosen
			-If used with <-s>, x samples with highest weight are chosen
		-o,--out	: Suffix for output file
			-Prefix will be formatted as: O+P3+P2+P1.$out for 4-taxon test
			-$out be default is 'compd'
		-h,--help	: Displays help menu


	Infile format:
		OUT1 OUT2 OUT3+OUT4
		P3A P3B
		P2A P2B P2C P2D P2D
		P1A P1B

	#Order follows that of Comp-D
	#Pop IDs will be used to create CompD infiles for all combinations````
