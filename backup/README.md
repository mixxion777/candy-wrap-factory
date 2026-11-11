# Original music backup

The source WAV is stored in 16 binary parts because the GitHub connector upload limit is smaller than this 11.8 MB file.

From this repository root in PowerShell, restore it with:

```powershell
Get-ChildItem backup/chip_jpop_song.wav.part* | Sort-Object Name | Get-Content -Encoding Byte | Set-Content dist/chip_jpop_song.wav -Encoding Byte
```
