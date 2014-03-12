codegoeshere
============
pdml2arff.py allows one to export the entire contents of a pcap file into an arff file (with the help of tshark creating a pdml).

There are a handful of applications and utilities which seem to export *some* of a pcap, but we  wanted ALLLLL of the pcap, not just parts of it.  You'll probably still have to do quite a bit of pre-processing to make any use of the data in Weka, but as far as I can tell this gives you a full pcap converted to Weka format (ARFF).

Here are the usage notes:

this script will take a tshark generated pdml file and turn it
into an arff formatted file, suitable for ingestment by weka
here's how to create the pdml file from pcap:
tshark -T pdml -r <infile> > <outfile>
(adding -V gets you no more data)
usage of this script: pdml2arff.py <outfile> (outfile is pdml from above you can call it <infile> if calling it <outfile> confuses you.  To be fair, it's the <infile> for pdml2arff.py, but it's the <outfile> from the previous step, so leaving the name at <outfile> seemed to make sense)

good luck!  Input and feedback much appreciated.
