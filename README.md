# Common-AudioUnit-V3
Utilities related to the new version 3 Audio Units

### SimplePlayEngine+Recording.swift

> Fred: As AuV3 developers, one of the first things I've needed is the ability to record the output of my App for signal analysing purposes or simply sampling.

SimplePlayEngine utility extension to manage recording of the main mixer node output to a file. The SimplePlayEngine class is provided by Apple in the sample [AudioUnitV3Example: A Basic AudioUnit Extension and Host Implementation"](
https://developer.apple.com/library/content/samplecode/AudioUnitV3Example/Introduction/Intro.html)

Usage (Swift):
```swift
if (!self.engine.isRecording) {
	self.engine.startRecording(toURL: URL(fileURLWithPath:"YOUR_PATH/output.aif"))
} else {
	self.engine.stopRecording()
}
```

Usage (Objective-C):
```objective-c
if (![engine isRecording]) {
	[engine startRecordingToURL: [NSURL URLWithString:@"YOUR_PATH/output.aif"]];
} else {
	[engine stopRecording];
}
```
