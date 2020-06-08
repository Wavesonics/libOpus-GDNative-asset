# Godot-Opus
libOpus for Godot
Ecode and Decode Opus to and from raw PCM data. This results in huge compression ratios, especially for audio data containing mostly speech. Often well over 100x compression.

This is intended to allow for transmittion of auto data over the internet from inside Godot, with an eye toward eventually enabling real-time VOIP.

## Usage
Once installed, remember to activate the plug in inside of Godot:
Project -> Project Settings -> Plugins
Then change "***Opus Codec***" to Active

This will add two new nodes to Godot:
- `OpusEncoder`
  - `encode(pcmData: PoolByteArray) -> PoolByteArray`
- `OpusDecoder`
  - `decode(opusPackets: PoolByteArray) -> PoolByteArray`

## Demos
### Trivial
A demo showing the round trip from PCM -> Opus -> PCM can be seen here:
The Godot project file in this repository provides a simple demo in `example/` for locally recording audio, encoding it, deecoding it, and playing it back.

**How to use:**
1) Press record button
2) Talk or what ever
3) Press stop
4) Press Encode
5) Press Decode/Player

### VOIP
And a demo showing how to implement a very simple VOIP system using Godot-Opus can be seen here:
https://github.com/Godot-Opus/godot-voip-opus-demo
