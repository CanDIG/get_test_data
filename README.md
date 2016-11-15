# get_test_data

Downloads a random 50 samples worth of test data (full VCFs, stub BAMs) from the thousand genome project; small modifications to the test data script that comes with the ga4gh server v0.3.4.

Copy the download_fuller_example_data.py script into the server-0.3.4/scripts directory, and get_n_samples above the server-0.3.4 directory; then run, eg:

`./get_n_samples /path/to/ga4gh/server-0.3.4 /path/to/output/dir`

Once this is done, editing config.py to contain `DATA_SOURCE=/path/to/output/dir/50_samples/registry.db` and restarting the server should work.

Requires:

- bcftools
- bgzip
- samtools
- sort
- tabix
- wget
- zcat
