# UV-ANIM-2.10-X64-FIX
Fixes UV animation support for version 2.10


This patch restores the correct handling of UV animation data by updating the affected instructions at:
0x25E598 – 0x25E5E8
0x25F49C – 0x25F4E8
The fix corrects the UVAnim data reads required for the animation system to properly process and apply UV transformations.

modified functions
RpMaterialUVAnimApplyUpdate
RpMaterialUVAnimApplyUpdate
Affected version: GTA SA Mobile 2.10
Architecture: ARM64 / 64-bit


    CHook::Write32(SA_Addr(0x25E598), 0xB9401668);
    CHook::Write32(SA_Addr(0x25E5A0), 0xB9401E68);
    CHook::Write32(SA_Addr(0x25E5AC), 0xB9401A68);
    CHook::Write32(SA_Addr(0x25E5BC), 0xB9402268);
    CHook::Write32(SA_Addr(0x25E5C4), 0xB9402668);
    CHook::Write32(SA_Addr(0x25E5E8), 0xBD401260);

    CHook::Write32(SA_Addr(0x25F49C), 0xB94016C8);
    CHook::Write32(SA_Addr(0x25F4A4), 0xB9401EC8);
    CHook::Write32(SA_Addr(0x25F4AC), 0xB9401AC8);
    CHook::Write32(SA_Addr(0x25F4C0), 0xB94022C8);
    CHook::Write32(SA_Addr(0x25F4C8), 0xB94026C8);
    CHook::Write32(SA_Addr(0x25F4E8), 0xBD4012C0);
