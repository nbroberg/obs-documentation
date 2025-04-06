# Complete Church Streaming Setup Guide

## Table of Contents
1. Initial Setup and Installation
2. YouTube Channel Setup
3. OBS Configuration
4. Scene Creation and Audio Setup
5. Going Live Process
6. During the Stream
7. Troubleshooting

## 1. Initial Setup and Installation

### Installing OBS
1. Visit https://obsproject.com/
2. Download and install for your operating system
3. Run the installation wizard with default settings
4. Launch OBS Studio

### Initial OBS Configuration
1. Run Auto-Configuration Wizard:
   - Tools → Auto-Configuration Wizard
   - Select "Optimize for streaming"
   - Follow the wizard's recommendations

## 2. YouTube Channel Setup

### One-time Channel Preparation
1. Verify your YouTube channel
   - Go to youtube.com/verify
   - Complete phone verification
   - Wait 24 hours for streaming activation

2. Enable live streaming
   - Access YouTube Studio
   - Click "Create" → "Go Live"

### Creating a Stream
1. In YouTube Studio:
   - Click "Create" → "Go Live"
   - Choose "Stream now" or "Schedule stream"

2. Configure Stream Settings:
   - Set title, description, and category
   - Upload thumbnail (1280x720)
   - Choose visibility (Public/Unlisted/Private)
   - Configure advanced settings (chat, DVR, latency)

## 3. OBS Configuration

### Stream Settings
1. Open OBS Settings → Stream
2. Configure:
   ```
   Service: YouTube - RTMP
   Server: Primary YouTube ingest server (auto)
   Stream Key: Copy from YouTube Studio
   ```

### Video Settings
1. Settings → Video:
   ```
   Base Resolution: 1920x1080
   Output Resolution: 1920x1080
   Downscale Filter: Lanczos
   FPS: 30 (or 60 if higher upload speeds available)
   ```

### Output Settings
1. Settings → Output:
   ```
   Encoder: x264 (or NVENC if available)
   Rate Control: CBR
   Bitrate: 4000-6000 Kbps
   Keyframe Interval: 2
   CPU Usage Preset: Very Fast
   Profile: High
   ```

## 4. Scene Creation and Audio Setup

### Main Service Scene Setup
1. Create scenes:
   - Pulpit Scene
   - Congregation Scene
   - Pre-Service Scene
   - Lower Thirds

2. Add standard sources:
   - Video Capture Device (cameras)
   - Audio Input Capture (microphones)
   - Image (church logo)
   - Text (service information)

### Audio Configuration
1. Pulpit Audio Setup:
   ```
   Filters (in order):
   1. Noise Suppression
      - Method: RNNoise
      - Intensity: Medium
   2. Compressor
      - Ratio: 4:1
      - Threshold: -18dB
      - Attack: 6ms
      - Release: 60ms
   ```

2. Congregation Audio Setup:
   ```
   Filters (in order):
   1. Noise Suppression
      - Method: RNNoise
      - Intensity: Light
   2. Compressor
      - Ratio: 2:1
      - Threshold: -24dB
      - Attack: 10ms
      - Release: 100ms
   ```

## 5. Going Live Process

### Pre-Stream Checklist
1. Technical Check (30 min before):
   ```
   □ Internet connection speed test
   □ Camera connections
   □ Audio levels
   □ Scene transitions
   □ Microphone tests
   ```

2. Content Check:
   ```
   □ Stream title/description
   □ Thumbnail uploaded
   □ Chat moderation setup
   □ Graphics prepared
   □ Schedule confirmed
   ```

### Launch Sequence
1. Start streaming in OBS
1. Verify stream health in YouTube Studio
1. Check preview feed
1. Click "Go Live" in YouTube Studio

## 6. During the Stream

### Active Monitoring
1. Stream health indicators
1. Audio levels
1. Chat engagement
1. System resources
1. Network stability

### Best Practices
1. Use dedicated streaming computer
1. Monitor stream on separate device
1. Keep support contact information handy
1. Prepare backup scenes

## 7. Troubleshooting

### Common Stream Issues
1. Dropped Frames
   - Check internet connection
   - Lower bitrate
   - Switch to backup internet

2. Audio Problems
   - Check audio sync offset
   - Verify filter settings
   - Monitor for feedback loops

3. YouTube-Specific Issues
   - Stream key validation
   - Account status verification
   - Chat functionality
   - Quality options processing

Remember to always perform a test stream before important events and maintain backup plans for technical difficulties.
