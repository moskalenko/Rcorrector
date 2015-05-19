Rcorrector
=========

Described in:

Rcorrrector includes program Jellyfish2 []()

### What is Rcorrector?

Rcorrector is a kmer-based error correction method for RNA-seq data. It 

### Install

1. Clone the [GitHub repo](https://github.com/mourisl/rcorrector), e.g. with `git clone https://github.com/mourisl/rcorrector.git`
2. Run `sh build.sh` in the repo directory

### Usage
	Usage: perl run_rcorrector.pl [OPTIONS]
	OPTIONS:
		Required
		-r STRING: the path to the sequence file. Can use multiple -r to specifiy multiple sequence files
		-p STRING STRING: the paths to the paired-end data set. Can use multiple -p to specifiy multiple sequence files
		-k INT: kmer_length
		Optional
		-od STRING: output_file_directory (default: ./)
		-t INT: number of threads to use (default: 1)
		-trim : allow trimming (default: false)
		-maxcor INT: the maximum number of correction every 100bp (default: 8)\n
		-maxcorK INT: the maximum number of correction within k-bp window (default: 4)
		-ek INT: expected_number_of_kmers; does not affect the correctness of program but affect the memory usage (default: 100000000); 


### Output
For each input file specified by "-r" or "-p", Rcorrector will generate the corresponding output file with "*.cor.fq/fa" in the directory specified by "-od".


### Example
perl run_rcorrector.pl -p frag_1.fq frag_2.fq -k 23 


### Terms of use

This program is free software; you can redistribute it and/or modify it
under the terms of the GNU General Public License as published by the
Free Software Foundation; either version 2 of the License, or (at your
option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received (LICENSE.txt) a copy of the GNU General
Public License along with this program; if not, you can obtain one from
http://www.gnu.org/licenses/gpl.txt or by writing to the Free Software
Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307  USA
 
### Support

Create a [GitHub issue](https://github.com/mourisl/rcorrector/issues).


