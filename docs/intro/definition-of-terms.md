# Definition of Terms <Badge text="Copied" type="warning"/>

**Apparent Trap**
:   The ability of one ink film to overprint another. Apparent trap is calculated through the following equation: Dop- D,/D2x 100, where D, equals the density of the first-down color, D, equals the density of the second-down color, and Dopequals the density of the overprint. All measurements are taken through the filter for the second-down color.

---

**Calibration**
:   Bringing a device or instrument to a known, repeatable setting for the purpose of standardizing the performance of the device.

---

**Characterization**
:   Documenting the color/image reproduction capabilities of a particular device under specific conditions.

---

**Chroma**
:   The degree of saturation of a color.

---

**CIE**
:   Commission Internationale de TEclairage (the International Commission on Illumination), an international standards-setting organization for colorimetry and related optical radiation measurements.

---

**CIE AE94**
:   A measure of color difference

---

**CIELAB**
:   A three-dimensional color space specified with Cartesian coordinates in which the vertical axis is lightness (L*) and the horizontal axes are a continuum of red/green (a*) and yellow/blue (b*). CIELAB serves as the profile connection space for many color management systems.

---

**CIELCH**
:   A three-dimensional color space specified in polar coordinates in which the vertical axis is lightness (L*), the distance from the neutral point is chroma (C*) and the hue is specified by polar angle.

---

**CIEXYZ**
:   Defines color in terms of three theoretical primaries, X, Y, and Z that are modeled on the human color response. Like LAB, XYZ can serve as the profile connection space for an ICC profile.

---

**Colorimetric Characterization**
:   Determining the color rendering abilities of device or system through spectral measurements of a specified sample of the rendered color gamut.

---

**Compensation Curve**
:   A cutback applied to a digital file to compensate for the tonal value increase of the printing system, either through application software or through a RIP.

---

**Color Management System**
:   Software used to generate color transforms between color rendering devices.

---

**Density**
:   The ability of a material to absorb light, expressed as the logarithm (base 10) of the opacity.

---

**Densitometric Characterization**
:   Determining the color rendering abilities of a device or system through density measurements of the process colors and their overprints.

---

**Densitometry**
:   Measurement of the light absorbing properties of an object.

---

**Dynamic Range**
:   The range of measurable values, from the lowest detectable amount to the highest.

---

**Gamut**
:   The range of different colors that can be produced by a device under specific conditions.

---

**Hue**
:   The general designation of color, such as “red,” “green,” or “purple,” specified by angular position around a circular color space.

---

**ICC**
:   The International Color Consortium which develops standards for the development of profile formats and procedures.

---

**Lightness**
:   The perception that an object emits or reflects more or less light, ranging from light to dark, or white to black. The vertical axis of the LAB and LCH color models.

---

**Linearization**
:   Moving toward a linear form, such that the input and ouput of a system remain the same.

---

**Optimization**
:   Determining the best combination of variables to produce the greatest desired result.

---

**PASOCCI**
:   A strategy for implementing consistent, predictable and repeatable color reproduction: prepare, analyze, stabilize, optimize, calibrate, characterize, implement.

---

**Photomechanical Characterization**
:   Another term for densitometric characterization Printability—the degree to which a substrate accepts ink with a minimum of distortion.

---

**Robust**
:   Vigorous, sturdy; a system that is consistent and durable. Spectrophotometry—measuring the reflectance or transmission of light energy at discrete intervals throughout the visible spectrum.

---

**Tonal Value Increase (TVI)**
:   Due to the physics of ink transfer to the substrate, the printed tones (expressed as dot percentage) are generally greater than the tones specified in the digital file; this difference is commonly referred to as dot gain. Tone Compression—the loss of detail in the reproduction due to the limited densities achievable by the printing system.

---

**Tone Reproduction**
:   In printing, creating the greatest range of densities through the application of ink to substrate via halftone dot percentages; ideally the greatest solid ink density without excessive TVI yields the best tone reproduction.

### More pulled from some rando TXT doc... Plagiarized?

Tristimulus Values--The amounts of three primary colored lights, which, when added, produce a visual, or "colorimetric" match with an original color. Such a set of primaries consists of the red, green, and blue phosphor colors of a TV tube, in which case the tristimulus values are called R, G, and B.

Appearance Signals--Values produced by any reversible transformation of RGB. Luminance/chrominance (LC1C2) and luminance, hue, and saturation (LHS) are two common sets.

Color--The specification of a colored stimulus requiring at least three component values.

Luminance--That aspect of a colored stimulus relating to its intensity.

Hue--That aspect of a colored stimulus relating to its color name.

Saturation--That aspect of a colored stimulus relating to its purity, or absence of contamination with white.

Chrominance--That aspect of a colored stimulus relating to its hue and saturation. The saturation is aproximately the ratio of chrominance amplitude to luminance.

Color Space--A three-dimensional space in which each point corresponds to a color, including both luminance and chrominance aspects. RGB form such a space. LHS form a set of cylindrical coordinates in color space. The L-axis is the diagonal of RGB space, so that L=0 where R=G=B=0, and L=max where R,G, and B are max. The C1C2 plane is perpendicular to the L-axis in LC1C2 space. The hue (angle) and chrominance (amplitude) are polar coordinates in the C1-C2 plane.

Lightness--A non-linear transformation of luminance in which equal increments are equally perceptible.

Density--The negative logarithm, to the base ten, of the reflectance or transmittance of a point in an image. In the case of colored inks or dyes, the density is measured through an appropriate color filter. The density is approximately proportional to the quantity of ink laid down. CMYK refer to the densities of cyan, magenta, yellow, and black ink normally used in printing.

Gamut--The range of colors producible with a set of inks, lights, or other colorants. The gamut can conveniently be described in terms of a particular region of a color space.

Transparent--That property of an optical medium such as a dye or an ink in which each ray of incident light is transmitted without change of direction, but attenuated (multiplied) by a factor which is always unity or less.

Standard Translation--When the reproduction gamut is smaller than the gamut of the original, the usual case, the dynamic range (contrast range) of the original must be compressed and in most cases, some highly saturated colors must be desaturated. Some special colors, such as skin tones, if they cannot be accurately reproduced, are preferably distorted in certain ways. All these changes, taken together, constitute the standard translation.

Color Mixture Curves (CMC's)--The spectral transmission curves for a set of color separation filters which produce signals which are tristimulus values with respect to a certain set of primaries.

Additive Mixture--The type of color mixture in which the light of each component is summed. A color TV tube has this type of mixture, which obeys particularly simple mixture rules.

Subtractive Mixture--The type of color mixture in which the spectral transmittance curves of the components multiply. Color films behave this way, approximately. The mixture rules are more complicated, but the resultant color can be accurately predicted. Ink mixtures as encountered in typical printing processes are more nearly subtractive than additive, but are extremely difficult to predict accurately because of non-ideal behavior of the inks.

Tone Scale Memory--A table implemented in digital hardware or in software which serves the purpose of a non-linear transformation. The addresses, typically 256, are the various levels of the input signal, while the contents, typically 8 bits at each location, are the corresponding levels of the output signal.

Colorimeter--An instrument or method for measuring the tristimulus values of arbitrary color samples.
