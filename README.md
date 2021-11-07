# Vortex2_Player_SJASM_ver2_compress_index
now added index of songs - code ripped from WYZ player

In UNCOMP_SONG, change the a register to the song you want to play

i.e.
ld a, 0; plays song 0
ld a, 1; plays song 1 etc...

UNCOMP_SONG:
	ld hl, TABLA_SONG_CMP
	ld a, 1; song number index starts at 0
	call EXT_WORD
	ld de, BUFFER_UNCOMP
	call dzx0_standard
	ret	
