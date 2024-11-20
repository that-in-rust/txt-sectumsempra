# txt-sectumsempra

A minimalistic file chunking utility that splits large text files into smaller chunks of equal size.

## Goal

Split a large text file into smaller chunks of equal size (N MB each).

## Product Requirements Document (PRD)

1. **Input**: Accept any text file regardless of size.
2. **Output**: Generate files of equal size of N MB each.
3. **Performance**: Process 1GB file in under 30 seconds.
4. **CLI Interface**: `cargo run absolute-path-input.txt size-in-MB` & output files will be placed in a new folder `input-start-timestamp` with names `input-part-0` to `input-part-N`.
5. **Validation**: Verify output files match input checksum.
