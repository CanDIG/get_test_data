# get_test_data

Downloads a random 50 samples worth of test data (full VCFs, stub BAMs) from the thousand genome project; small modifications to the test data script that comes with the ga4gh server v0.3.4.

Copy the download_fuller_example_data.py script into the server-0.3.4/scripts directory, and get_n_samples above the server-0.3.4 directory; then run ./get_n_samples

Requires:

- bcftools
- bgzip
- samtools
- sort
- tabix
- wget
- zcat
