# FreeU_Advanced
 FreeU - Free Lunch, and Dinner.
 
![image](https://github.com/WASasquatch/FreeU_Advanced/assets/1151589/b68e2830-9110-4497-a0a5-e5b24cc6e012)

## Input Parameters

- `model` (`MODEL`): Model to patch
- `multiscale_mode` (`COMBO`): A list of available multiscale modes:
  - `["Default", "Bandpass", "Low-Pass", "High-Pass", "Pass-Through", "Gaussian-Blur", "Edge-Enhancement", "Sharpen", "Multi-Bandpass", "Multi-Low-Pass", "Multi-High-Pass", "Multi-Pass-Through", "Multi-Gaussian-Blur", "Multi-Edge-Enhancement", "Multi-Sharpen"]`
- `multiscale_strength` (`FLOAT`, Default: 1.0, Range: [0.0, 1.0], Step: 0.001): Strength of scaling
- `b1` (`FLOAT`, Default: 1.1, Range: [0.0, 10.0], Step: 0.001): `b1`  output multiplier
- `b2` (`FLOAT`, Default: 1.2, Range: [0.0, 10.0], Step: 0.001): `b2`  output multiplier
- `s1` (`FLOAT`, Default: 0.9, Range: [0.0, 10.0], Step: 0.001): `s1` Fourier transform scale strength
- `s2` (`FLOAT`, Default: 0.2, Range: [0.0, 10.0], Step: 0.001): `s2` Fourier transform scale strength

### Optional Parameters

- `b1_mode` (`COMBO`): Blending modes for `b1` multiplied result.
  - `['bislerp', 'colorize', 'cosine interp', 'cuberp', 'hslerp', 'inject', 'lerp', 'linear dodge', 'slerp']`
- `b1_blend` (`FLOAT`, Default: 1.0, Range: [0.0, 100], Step: 0.001): Blending strength for `b1`.
- `b2_mode` (`list` of `str`): Blending modes for `b2` multiplied result.
  - `['bislerp', 'colorize', 'cosine interp', 'cuberp', 'hslerp', 'inject', 'lerp', 'linear dodge', 'slerp']`
- `b2_blend` (`FLOAT`, Default: 1.0, Range: [0.0, 100], Step: 0.001): Blending strength for `b2`.
- `threshold` (`FLOAT`, Default: 1.0, Range: [0.0, 1.0], Step: 0.001): The exposed threshold value of the Fourier transform function.
- `override_scales` (`STRING`, Default: [Multiline String]): Override scales. Create custom scales and experiment with results.
  - Example `10, 1.5` would create the `multiscale_mode` effect `Sharpen` 