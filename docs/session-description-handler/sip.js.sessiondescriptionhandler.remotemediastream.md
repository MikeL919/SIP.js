<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [sip.js](./sip.js.md) &gt; [SessionDescriptionHandler](./sip.js.sessiondescriptionhandler.md) &gt; [remoteMediaStream](./sip.js.sessiondescriptionhandler.remotemediastream.md)

## SessionDescriptionHandler.remoteMediaStream property

The remote media stream currently being received.

<b>Signature:</b>

```typescript
get remoteMediaStream(): MediaStream;
```

## Remarks

The remote media stream initially has no tracks, so the presence of tracks should not be assumed. Furthermore, tracks may be added or removed if the remote media changes - for example, on upgrade from audio only to a video session. At any given time there will be at most one audio track and one video track (it's possible that this restriction may not apply to sub-classes). Use `MediaStream.onaddtrack` or add a listener for the `addtrack` event to detect when a new track becomes available: https://developer.mozilla.org/en-US/docs/Web/API/MediaStream/onaddtrack
