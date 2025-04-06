# Complete Church Streaming Setup Guide

## Table of Contents

1. [Initial Setup and Installation](#initial-setup-and-installation)
2. [YouTube Channel Setup](#youtube-channel-setup)
3. [OBS Configuration](#obs-configuration)
4. [Scene Creation and Audio Setup](#scene-creation-and-audio-setup)
5. [Going Live Process](#going-live-process)
6. [During the Stream](#during-the-stream)
7. [Troubleshooting](#troubleshooting)

## Initial Setup and Installation

### Installing OBS

1. Visit https://obsproject.com/
2. Download and install for your operating system
3. Run the installation wizard with default settings
4. Launch OBS Studio

### Initial OBS Configuration

1. Run Auto-Configuration Wizard:
   - Tools → Auto-Configuration Wizard
   - Select `Optimize for streaming`
   - Follow the wizard's recommendations

## YouTube Channel Setup

### One-time Channel Preparation

1. Create a unit-specific [Google account](https://support.google.com/youtube/answer/161805) (if not already created):

   - Use format: unitname@gmail.com
   - Store credentials securely
   - Share with leadership team

2. [Create YouTube channel](https://support.google.com/youtube/answer/1646861):

   > See [Asheville Ward YouTube channel](https://studio.youtube.com/channel/UC8GiMLF9tS1041MliykYozA) for reference

   - Sign in to YouTube
   - Click profile icon
   - Select `Create a channel`
   - Choose `Create a custom name`
   - Enter unit name

3. Verify your YouTube channel

   - Go to youtube.com/verify
   - Complete phone verification
   - Wait 24 hours for streaming activation

4. Enable live streaming
   - Access YouTube Studio
   - Click `Create` → `Go Live`

### Logging into YouTube

1. Go to YouTube Studio:
   - Open your web browser
   - Navigate to studio.youtube.com
   - Sign in with your Google account

### Creating and Selecting Stream

1. Open OBS Settings → Stream:

   - Select `YouTube - RTMP` as Service
   - Click `Connect Account`
   - Follow browser prompts to link YouTube
   - Click `Apply` and `OK`

2. Configure Stream Information:

   - Click `Start Streaming`
   - In the browser window that opens:
     - Set title (example: `Unit Sacrament Meeting - [Date]`)
     - Set visibility to `Unlisted`
     - Upload thumbnail if desired
     - Click `Go Live`

3. Verify Stream:
   - Check `Stream Status` in OBS shows `Good`
   - Preview stream in YouTube Studio tab
   - Confirm audio levels are registering

## OBS Configuration

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
   CPU Usage Preset: Very Fast (depending on processor)
   Profile: High
   ```

## Scene Creation and Audio Setup

### Main Scene Setup

1. Create the following scenes:

   - Pulpit (main speaking scene)
   - Sacrament (wait scene for sacrament administration)
   - Stage (wide view)
   - Congregation (audience view)

2. Example audio and video sources for each scene:
   - Video Source: `Coax Chapel Cam`
     ```
     Resolution: 1920x1080 (recommended)
     FPS: 30 (or 60 if higher upload speeds available)
     ```
   - Audio Sources:
     - Filtered Audio (for pulpit)
     - Unfiltered Audio (for congregation)

### Audio Configuration

1. Basic Audio Setup:

   ```
   Filtered Audio (Pulpit):
   - Volume: ~49% (-6dB)
   - Noise Suppression Filter enabled

   Unfiltered Audio (Congregation):
   - Volume: 100% (0dB)
   ```

### Sacrament Scene Setup

1. Add sources:
   - Background Image (sunrise-field.png)
   - Text overlay with message:
     `Our broadcast will resume
after the administration of
the sacrament is complete.`

## Going Live Process

### Pre-Stream Checklist

1. Technical Check (30 min before):

   ```
   □ Internet connection speed test
   □ Camera connections
   □ Audio levels
   □ Scene transitions
   □ Microphone tests (for each scene)
   ```

2. Content Check:
   ```
   □ Stream title/description
   □ Thumbnail uploaded
   □ Graphics prepared
   □ Schedule confirmed
   ```

### Launch Sequence

1. Start streaming in OBS
1. Verify stream health in YouTube Studio
1. Check preview feed
1. Click `Go Live` in YouTube Studio

## During the Stream

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

## Troubleshooting

### Common Stream Issues

1. [Dropped Frames](https://streamshark.io/obs-guide/stopping-dropped-frames)

   - Check internet connection
   - Lower bitrate
   - Switch to backup internet

2. [Audio Problems](https://www.youtube.com/watch?v=4YOkWU9r5x4&ab_channel=MichaelFeyrerJr.)

   - Check audio sync offset
   - Verify filter settings
   - Monitor for feedback loops
   - Check physical connections

3. YouTube-Specific Issues

   - Stream key validation
   - Account status verification
   - Quality options processing

Remember to always perform a test stream before important events and maintain backup plans for technical difficulties.
