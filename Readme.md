# Sparkzstd
This is a decompressor for the Zstandard compression format (Original Documentation[https://github.com/facebook/zstd/blob/dev/doc/zstd_compression_format.md]

This is still work in progress but it can already decompress some files correctly.

## What are the goals of this project
Well mainly I had some time on my hands and wanted to write something that might be useful to someone out there.
The goal is to provide a io.Reader compatible API for reading zstd encoded data from a provided io.Reader.

## What is still missing
Generally all concepts of the Format have been implemented and are working (to a degree, some subtle bugs are still there)
1. Good benchmarks
2. Better doc
3. Bugfixing

## Which bugs are known
I am testing this on a few files right know
1. A simple .jpg which I cant upload here for copyright reasons. 
This already decodes correctly but it is also just 36kb big
2. A ubuntu 18.04.2-live-server-amd64.iso with md5sum: fcbcc756a1aa5314d52e882067c4ca6a. 
This decodes almost correctly. The result has the correct length but differs in about 400 bytes in different locations
