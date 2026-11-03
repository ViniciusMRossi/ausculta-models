# ausculta-models

Speech model files downloaded by the Ausculta app (offline transcription of
veterinary consultations). Nothing here is modified.

**Model:** Parakeet TDT 0.6B v3 by NVIDIA
(<https://huggingface.co/nvidia/parakeet-tdt-0.6b-v3>), converted to ONNX
int8 by the sherpa-onnx project (k2-fsa,
<https://github.com/k2-fsa/sherpa-onnx>).

**Source:** `sherpa-onnx-nemo-parakeet-tdt-0.6b-v3-int8.tar.bz2` from
<https://github.com/k2-fsa/sherpa-onnx/releases/tag/asr-models>, SHA-256
`5793d0fd397c5778d2cf2126994d58e9d56b1be7c04d13c7a15bb1b4eafb16bf`.
`encoder.int8.onnx`, `decoder.int8.onnx`, `joiner.int8.onnx` and
`tokens.txt` are extracted from it byte for byte, so the app never unpacks
an archive. `manifest.json` lists each file's size and SHA-256; the app
carries its own copy and refuses any file that does not match it.

**License:** Creative Commons Attribution 4.0 International (CC BY 4.0),
<https://creativecommons.org/licenses/by/4.0/>. Attribution: NVIDIA
(model) and k2-fsa / sherpa-onnx (ONNX conversion).

Made with `tool/models/publish_models.ps1` in the Ausculta repository.
