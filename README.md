# get_test_data

Contains two scripts: `./get_n_samples` which, as a test, downloads
a random 50 samples worth of test data (full VCFs, stub BAMs) from
the thousand genome project; and `./get_my_samples` which downloads 
a full 1/3 (834 samples) of the thousand genome project.  Drives
a python script which is a small modification to the test data
script that comes with the ga4gh server v0.3.4.

Download these files and copy the download_fuller_example_data.py script into the server-0.3.4/scripts directory.
Test the process with 50 samples by running, _e.g._

`./get_n_samples /path/to/ga4gh/server-0.3.4 /path/to/output/dir`

this will take about 5.5 hours and require about 3GB.  Once this
is done, editing config.py to contain
`DATA_SOURCE=/path/to/output/dir/50_samples/registry.db` and
restarting the server will serve up the data set.

To download the full 1000 genomes partition, run

`./get_my_samples /path/to/ga4gh/server-0.3.4 /path/to/output/dir HSC`

with `HSC` being replaced by `UHN` or `CQ` as appropriate for yours ite.

Requires on your server:

- bcftools
- bgzip
- samtools
- sort (Mac OS X: gsort)
- tabix
- wget
- zcat (Mac OS X: gzcat)
