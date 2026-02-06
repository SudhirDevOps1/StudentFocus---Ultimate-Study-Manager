# 🎵 Music Guide for StudentFocus

## Adding Your Own Music

The StudentFocus app includes a built-in music player that looks for music files in the `/music` folder. To add your own focus music:

### 1. Music Folder Structure
```
your-app-folder/
├── music/
│   ├── focus-flow.mp3
│   ├── deep-concentration.mp3
│   ├── calming-mind.mp3
│   ├── productive-pulse.mp3
│   └── silent-study.mp3
└── old_index.html
```

### 2. Adding Your Music Files

1. Place your MP3 files in the `music/` folder
2. Make sure the filenames match what's in the code:
   - `focus-flow.mp3`
   - `deep-concentration.mp3`
   - `calming-mind.mp3`
   - `productive-pulse.mp3`
   - `silent-study.mp3`

### 3. Replacing the Placeholder Files

To add your own music:

1. Navigate to the `music/` folder
2. Replace the placeholder files with your own MP3 files
3. Keep the same filenames to ensure the app recognizes them

### 4. Supported Audio Formats

Currently, the app is configured to use MP3 files. You can also use other formats like:
- `.mp3` (recommended)
- `.ogg`
- `.wav`

### 5. Audio Quality Recommendations

- Use audio files with a bitrate of 128kbps or higher for better quality
- Keep file sizes reasonable to ensure quick loading
- Focus music should ideally be instrumental or ambient sound

### 6. Customizing the Playlist

If you want to add more tracks or change the default ones:

1. Edit the `musicTracks` array in `old_index.html` around line 3450
2. Add or modify entries with the correct file paths
3. Update the UI elements to reflect your changes

### 7. Troubleshooting

If music isn't playing:

1. Check that the music files are in the correct folder
2. Verify the filenames match exactly what's in the code
3. Ensure the files are valid MP3 files
4. Check browser console for any error messages
5. Make sure your browser supports HTML5 audio

---

**Note:** The music player is designed to enhance your focus while studying. Choose instrumental or ambient music without distracting lyrics for best results.