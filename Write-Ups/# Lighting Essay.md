# Lighting Essay

## Measuring light

- lighting is physically based so that real values can be used, avoiding guessing.
- light measuring
  - lumens measures the total amount of light energy emitted by a source in all directions
    - bulb 800 lumens
    - candle 12 lumens
    - lumens used for rectangular lights because they emit light from an area
  - candelas (cd) is the light intensity in one direction
    - used for point lights, spotlights and directional light
  - lux measures how much light hits a surface
  - nits measure how bright a surface appears
    - light coming from a surface such as a monitor or phone screen 

## Exposure

- aperture, ISO, shutter speed
- UE5 simulates exposure adaptation

| **Section** | **Notes** |
| --- | --- |
| Exposure | - aperture, ISO, shutter speed <br> - UE5 simulates exposure adaptation <br> - Post process exposure and apeture ect can be adjust through post process volume or on each individual camera |
| Temperature | - temperature sets a more accurate colour than light colour settings |
| Directional Light | - all light rays are parallel to each other as if the light is infinitely far away <br> - creates cascaded shadow maps or virtual shadow maps <br> - The light itself is cheap but the shadows are expensive |
| Mobility | - static lights, completely backed into lightmaps, cannot move or change at runtime <br> - stationary, hybrid, indirect lighting is backed but can still affect things like character shadow <br> - dynamic light, runtime light |
| skylight | - fills the entire area with the colour of the cubemap <br> - recapture takes a 'screenshot' of the sky and tints the world the colour of the sky |
| Spot lights |  |
| Rectangle lights | - can input a source texture, light colour will change to match, could use for a tv video and the light will adjust <br> - expensive light so should use sparingly |
| Baked lighting | can get higher quality lighting compared to Lumen if done right <br> Use a separate UV channel cannot have overlapping UVs |
| render settings | - use hardware ray tracing when available on raytracing is very expensive so specific chips in graphics cards are needed to run <br> |
| Lumen | creates simplified geometry and saves this in cache stores lighting information for surfaces in world space, uses fast screen space traces, for off screen geometry Lumen traces |

