# Y2JB Lapse Exploit - Stable+ Improvements

## Overview

This is an improved version of the Y2JB (YouTube to Jailbreak) Lapse exploit with **carefully tuned parameters** for better reliability on PS5 firmware 8.40.

## What Changed

### Optimized Parameters

The following parameters were increased by **20-25%** to improve success rate while maintaining stability:

| Parameter | Original | Stable+ | Change |
|-----------|----------|---------|--------|
| `NUM_RACES` | 100 | 120 | +20% |
| `NUM_ALIAS` | 100 | 120 | +20% |
| `NUM_LEAKS` | 16 | 20 | +25% |

### What Stayed the Same

All other parameters remain at their original values to ensure stability:
- `NUM_GROOMS`: 512 (unchanged)
- `NUM_HANDLES`: 256 (unchanged)
- `NUM_SDS`: 64 (unchanged)
- `NUM_SDS_ALT`: 48 (unchanged)
- `NUM_CLOBBERS`: 8 (unchanged)
- `MAX_AIO_IDS`: 128 (unchanged)

## Results

**Tested Success Rate:** 5/5 (100%) on PS5 FW 8.40

The improvements provide:
- ✅ Better success rate (fewer retries needed)
- ✅ Maintained stability (no crashes or hangs)
- ✅ Same timing characteristics as original

## Why These Changes Work

1. **NUM_RACES/NUM_ALIAS (+20%)**: Provides more attempts for the race condition without overwhelming the kernel heap
2. **NUM_LEAKS (+25%)**: Increases chances of successful kernel address leak
3. **Conservative approach**: Small incremental changes prevent timing issues that larger changes caused

## Installation

Use the provided `y2jb_update.zip` file with the Y2JB autoloader update mechanism.

## Credits

- Original Lapse exploit: anonymous, Gezine
- Optimization: Based on careful analysis and testing
- Y2JB Autoloader: itsPLK

## Version

**Y2JB Lapse 1.0 Stable+ (Minor Improvements)**

## Compatibility

- PS5 Firmware: 8.40
- Y2JB Autoloader: Latest version from itsPLK repository
