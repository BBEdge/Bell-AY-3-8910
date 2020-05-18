#### Bell-AY-3-8910

```
CPU 8085
GAL ATF16V  
DAC AY-3-8910
```

#### LOGIC
```
/** Inputs **/
Pin 1 = CLK;
Pin 2 = IOM;
Pin 3 = RD;
Pin 4 = WR;
Pin 5 = A14;
Pin 6 = A15;

/** Outputs **/
Pin 16 = RAM_CS;
Pin 17 = ROM_CS;
Pin 18 = BC1;
Pin 19 = BDIR;

/** IOM Logic **/
!BC1 = !A14 # !IOM;
!BDIR = WR # !IOM;
!ROM_CS = !A15 & !IOM;
!RAM_CS = A15 & !IOM;
```
