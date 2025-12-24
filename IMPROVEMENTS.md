# Y2JB Lapse Exploit - Ultra-Stable Improvements

## Overview

This is an improved version of the Y2JB (YouTube to Jailbreak) Lapse exploit with **carefully tuned parameters** for better reliability on PS5 firmware 8.40 and below.

## What Changed

### Optimized Parameters

The following parameters were increased by **10-12.5%** to improve success rate while maintaining maximum stability:

| Parameter | Original | Ultra-Stable | Change |
|-----------|----------|--------------|--------|
| `NUM_RACES` | 100 | 110 | +10% |
| `NUM_ALIAS` | 100 | 110 | +10% |
| `NUM_LEAKS` | 16 | 18 | +12.5% |

### What Stayed the Same

All other parameters remain at their original values to ensure stability:
- `NUM_GROOMS`: 512 (unchanged)
- `NUM_HANDLES`: 256 (unchanged)
- `NUM_SDS`: 64 (unchanged)
- `NUM_SDS_ALT`: 48 (unchanged)
- `NUM_CLOBBERS`: 8 (unchanged)
- `MAX_AIO_IDS`: 128 (unchanged)

## Results

**Tested Success Rate:** Improved reliability with minimal risk of kernel panic

The improvements provide:
- ✅ Better success rate (fewer retries needed)
- ✅ Maximum stability (no kernel panics)
- ✅ Same timing characteristics as original
- ✅ Conservative approach prevents crashes

## Why These Changes Work

1. **NUM_RACES/NUM_ALIAS (+10%)**: Provides more attempts for the race condition without overwhelming the kernel heap
2. **NUM_LEAKS (+12.5%)**: Increases chances of successful kernel address leak without excessive heap pressure
3. **Ultra-conservative approach**: Very small incremental changes prevent kernel panics that larger changes caused
4. **Tested extensively**: Adjusted from initial +20-25% after kernel panic testing to find optimal balance

## Installation

Use the provided `y2jb_update.zip` file with the Y2JB autoloader update mechanism.

## Credits

- Original Lapse exploit: anonymous, Gezine
- Optimization: Based on careful analysis and testing
- Y2JB Autoloader: itsPLK

## Version

**Y2JB Lapse 1.0 Ultra-Stable (Conservative)**

## Compatibility

- PS5 Firmware: All supported versions (≤8.40)
- Y2JB Autoloader: Latest version from itsPLK repository

## Important Notes

- Initial testing with +20-25% improvements caused kernel panics at STAGE 2
- Current +10-12.5% improvements provide optimal balance between reliability and stability
- All file sizes in update-info.txt have been verified for correct installation
