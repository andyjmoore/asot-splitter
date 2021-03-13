# A State of Trance Splitter Util
Takes ASOT episodes from the Youtube channel, and converts the tracklist into a cue sheet for splitting up into separate audio tracks.
Tools used:
- 4K YouTube To MP3 - rips the YouTube vid to mp3
- Audacity - for UI layer on saving the ripped mp3 to WAV. !! Make sure the sampling rate is set to 44100 before exporting, otherwise CUETools will complain later!
- this util - convert the YouTube vid details tracklist format to the cue sheet format
- CUETools - spitting the ripped WAV per the cue sheet

## Usage
1. Open asot-splitter.html locally in a browser.
2. Copy the ASOT tracklist from its associated YouTube entry on [Armin van Buuren's YouTube channel](https://www.youtube.com/channel/UCu5jfQcpRLm9xhmlSd5S8xw).
3. Paste the ASOT tracklist into the "Tracklist" field on the page, and use the "Transform" button to produce the cue sheet output in the "Cue sheet output" field.
4. Copy the cue sheet output into a .cue file. Use that CUETools, plus the WAV version of ASOT episode YouTube video, to produce the split tracks.

## Handling Long Episodes
CUETools doesn't handle CUE sheets that go much beyond 2 hrs. For extended ASOT episodes (3hrs with bonus sets, or 4hr end-of-year roundups), these are currently handled as follows:
1. When creating the CUE sheet, this tool will output a concatenated series of CUE sheets in the output, with each lasting no more than 2h5m.
2. When creating the WAV files, split into multiple WAVs in line with the split CUE sheets.