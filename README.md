# AGCobra GGUF Header Notes

[Gemma Pirate GGUF Header Viewer](https://huggingface.co/spaces/AGCobra/gemma-gguf-header-viewer) is a small browser utility for inspecting the fixed header prefix of a public GGUF file.

It requests bytes 0–23 of `gemma-4-12b-it-pirate.Q8_0.gguf` from [AGCobra/Gemma-12b-it-Pirate](https://huggingface.co/AGCobra/Gemma-12b-it-Pirate), pinned to revision `3887a7cd753f26397b1d95c45a84fe8e7064d58d`. Press **Read GGUF header** to see the format version, tensor count, metadata-entry count, and raw prefix bytes.

The viewer validates the expected partial response and reads the fixed fields in little-endian order. It does not perform inference or load tensor weights. The displayed counts describe the prefix; the utility does not parse the remaining metadata values or variable-length header.
