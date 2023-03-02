# TP600_Sound
WAGO TP600 Control Panels have a built-in mini-jack audio port. There is possibility to play wav files from Codesys runtime.
Added **sound** bash script allows to play, stop, restart, get status of the currently played song.

## Instruction
1. Copy *.wav files to /home/ folder (using ftp or ssh Filezilla/WinSCP)
2. Copy program **sound** to */etc/config-tools/*
3. Connect by SSH ([Putty](https://putty.org/)) and add execute permission:

       chmod +x /etc/config-tools/sound
       
## e!COCKPIT/Codesys 3.5
1. Add *WagoAppConfigTool* library
2. Use FbConfigTool, as *sCallString* use: 

       sCallString: STRING := './sound start /home/<sound_file>.wav';
       sCallString: STRING := './sound stop';
       sCallString: STRING := './sound restart';
       sCallString: STRING := './sound status';
