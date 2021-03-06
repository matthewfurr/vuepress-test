# Color Management <Badge text="Copied" type="warning"/>

## From Rando TXT File

Color is not subjective: Every color that can be printed can also be measured, and it characteristics stored as a spectral curve that acts as the "DNA" of the color and serves as an exact specification for further reproduction.

## From O'Hara

Color management systems were developed in the late 1980s and early 1990s in
response to the need for more flexible color transforms than had been traditionally available (Fraser, Murphy & Bunting, 2003). Digital prepress systems rapidly became more widespread as the computational power of computers increased and the cost of computers decreased. Image manipulation software and low-end scanners became affordable to a wide range of designers and clients, and as desktop publishing systems became more available, prepress professionals had to receive input from and purpose images for a much broader range of devices. In the traditional printing model,  transparencies were provided to scanner operators who had control over the color conversion to a digital format. High-end photo-multiplier tube (PMT) drum scanners were the industry standard for color separation, and the separation settings were built into the image capture by the scanner operators. These “closed loop” systems were carefully calibrated to produce separations for specific printing conditions. Ink densities, dot gain curves and gray balance information were determined through densitometric evaluation of press characterizations, and images were converted from the RGB input of the scanner capture to the CMYK of a specific printing system on the fly. In a closed loop, the image capture settings are specific for the intended output device, and repurposing an image to other devices meant rescanning the image to create separations for each output (Sharma, 2004). In contrast, a color management system provides a relatively simple means of converting color between a multitude of devices.

Color management systems (CMS) use device profiles to quantify the color reproduction capabilities of the various components of the color reproduction system. The profile is essentially a look-up table between input to the color rendering component and the output from that component, relating digital information to actual color. For instance, in the case of a scanner or digital camera, the input to the system is the actual colors of the image or object being captured, and the output is the digital RGB values for each pixel comprising the image. For a press or a proofing device, the input is the digital information of the file (CMYK dot percentages) and the output is the actual colors of the printed sheet. The actual color can be quantified through spectral measurement; with a standard light source (D50 or D65) and a standard observer specified (2° or 10° observer), the spectral reflectance of the object defines the color. Using the spectral reflectance data and the spectral properties of the light source (D50 or D65) and the observer function (2° or 10°), the color can be rendered into an independent color space such as CIEXYZ or CIELAB. CIELAB is an independent color space in which colors are mapped onto three- dimensional axes of light/dark (L*), red/green (a*) and yellow/blue (b*). In most color management systems, either CIELAB or CIEXYZ serves as the profile connection space (PCS), a common currency to allow color transformations between color devices. Each device renders colors through the application of colorants—in the case of a press, the colorants are applied in dot percentages of CMYK; for a scanner or digital camera, the colorants are RGB pixels. These colorants are the ingredients each device uses to create specified colors; the specific combinations of CMYK/RGB may be thought of as recipes. The profile for each device is a look-up table between all the colors that device can render, as specified in CIELAB, to the recipes the device requires for each color. In this way, the CMS can relate each device in a color reproduction system to CIELAB, the profile connection space. The PCS serves as a digital hub for color transforms; instead of relating each device to each other in a series of one-to-one, closed-loop relationships, each device is related to the PCS, and from the PCS color transforms can be accomplished to any device that has a profile in the color management system. Figure 6, The Profile Connection Space, illustrates how color-rendering devices are linked through the PCS via their profiles.

Profiles are created by putting known color input into the color rendering device and measuring the resulting output. For example, scanners and digital camera, which serve as input devices for the color reproduction system, are profiled by capturing a color target with known LAB values and measuring the RGB values that result from the image capture (Sharma, 2004). In each case, the color of the object is transformed into RGB pixels by using filters to separate the image. All filters are not the same, and different devices will derive different RGB pixels. The profile relates the input LAB to the resulting RGB pixels. As it is impractical to capture every possible color, color management systems use color targets that are comprised of a strategically selected sample of color representing an array of hues at various lightness and chroma levels. The profile creation software then performs a series of computations that interpolate between the sampled colors to create a look-up table to provide “recipes” for all of the colors that the device is capable of producing.

In the case of printing systems, the input to the system is the digital CMYK dot percentage values and the output is the color that results. As previously discussed in the introduction, the color that results is dependent on a number of factors such as which pigments are used, the pigment load, the ink film thickness printed, the color properties of the substrate, printability issues like ink hold-out, surface smoothness, the degree of impression, apparent trap, tonal value increase, and many, many other variables involved in the application of the ink to the substrate. To create the profile for a printing system, a look-up table is generated by printing a strategic sample of the possible CMYK input values and measuring the LAB colors that are output. From the sample, the gamut of the printing system is determined and CMYK “recipes” are interpolated for all of the colors within the gamut of the printing system.

## Colorimetric Characterization with Compensation for TVI

In a preface to a 2001 IT8.7/4 proposal, David McDowell states that “the CMYK ink values specified are those to used as input to the printing processes; no additional normalization or ‘cutback’ curves should be applied” (McDowell, 2001). This intention is further documented in CGATS/SC4 N 406, How to run a good press testfor development of a color characterization data set (Draft 2), which states, “tone reproduction on separation films and on digitally imaged plates should have a final linear relationship to the original data file” (CGATS/SC4 N 406 draft 2). However, others have proposed alternative approaches to the characterization. The third edition of the Flexographic  Image Reproduction Specifications and Tolerances (FIRST) recommends that colorimetric characterization is best performed if the printing system is calibrated for a specific amount of TVI—17% midtone gain, such that the 50% tint prints as a 67% tint (FIRST, 2003). FIRST claims that this amount of TVI will provide the best distribution of colorimetric data from an IT8.7/4 target. In a presentation at the FFTA’s 2003 FIRST conference, Mark Samworth of Artwork Systems, Inc. advocated the use of TVI compensation with ICC profiling, particularly for flexography, which typically has higher TVI than offset lithography. In this presentation, Samworth suggested that by taking the adjustment for TVI away from the profile, the profile does not have to “move” the color as much. TVI is a one-dimensional change that can be best addressed through a compensation curve, while the colorimetric properties of the inks and their overprints are best addressed through a profile (Samworth, 2003). Samworth further argued that the compensated target provides better highlight sampling for improved color transforms.

Currently, there is no published experimental study on the effectiveness of applying compensation curves to characterizations in order to improve color reproduction. This research was undertaken to examine whether or not calibrating a printing system to specified amounts of TVI would result in a more evenly distributed colorimetric sampling, and whether or not the distribution of the colorimetric sampling would have an impact on the color reproduction accuracy of profiles generated from such data.

## CIE76

Given two colors in CIELAB color space, $\left(L_{1}^{*}, a_{1}^{*}, b_{1}^{*}\right)$ and $\left(L_{2}^{*}, a_{2}^{*}, b_{2}^{*}\right)$, the $\mathrm{CIE} 76$ color difference formula is defined as:

$\Delta E_{a b}^{*}=\sqrt{\left(L_{2}^{*}-L_{1}^{*}\right)^{2}+\left(a_{2}^{*}-a_{1}^{*}\right)^{2}+\left(b_{2}^{*}-b_{1}^{*}\right)^{2}} .$

$\Delta E_{a b}^{*} \approx 2.3$ corresponds to a JND (just noticeable difference).

## CIE94

The 1976 definition was extended to address perceptual non-uniformities, while retaining the CIELAB color space, by the introduction of application-specific weights derived from an automotive paint test's tolerance data.

ΔE (1994) is defined in the L\*C\*h\* color space with differences in lightness, chroma and hue calculated from L\*a\*b\* coordinates. Given a reference color $\left(L_{1}^{*}, a_{1}^{*}, b_{1}^{*}\right)$ and another color $\left(L_{2}^{*}, a_{2}^{*}, b_{2}^{*}\right)$, the difference is:

$\Delta E_{94}^{*}=\sqrt{\left(\frac{\Delta L^{*}}{k_{L} S_{L}}\right)^{2}+\left(\frac{\Delta C_{a b}^{*}}{k_{C} S_{C}}\right)^{2}+\left(\frac{\Delta H_{a b}^{*}}{k_{H} S_{H}}\right)^{2}}$

where:

$\begin{aligned}
\Delta L^{*} &=L_{1}^{*}-L_{2}^{*} \\
C_{1}^{*} &=\sqrt{a_{1}^{*}{ }^{2}+b_{1}^{*}} \\
C_{2}^{*} &=\sqrt{a_{2}^{* 2}+b_{2}^{* 2}} \\
\Delta C_{a b}^{*}  &=C_{1}^{*}-C_{2}^{*} \\
\Delta H_{a b}^{*} &=\sqrt{\Delta E_{a b}^{*}{ }^{2}-\Delta L^{* 2}-\Delta C_{a b}{ }^{2}}=\sqrt{\Delta a^{* 2}+\Delta b^{* 2}-\Delta C_{a b}^{*}{ }^{2}} \\
\Delta a^{*} &=a_{1}^{*}-a_{2}^{*} \\
\Delta b^{*} &=b_{1}^{*}-b_{2}^{*} \\
S_{L} &=1 \\
S_{C} &=1+K_{1} C_{1}^{*} \\
S_{H} &=1+K_{2} C_{1}^{*} \end{aligned}$

and where $k_{C}$ and $k_{H}$ are usually both unity and the weighting factors $k_{L}, K_{1}$ and $K_{2}$ depend on the application:

|         | graphic arts |
| ------- | ------------ |
| $k_{L}$ | 1            |
| $K_{1}$ | 0.045        |
| $K_{2}$ | 0.015        |

Geometrically, the quantity $\Delta H_{ab}^{*}$ corresponds to the arithmetic mean of the chord lengths of the equal chroma circles of the two colors.

## CIEDE2000

Since the 1994 definition did not adequately resolve the perceptual uniformity issue, the CIE refined their definition, adding five corrections:

- A hue rotation term ($R_{T}$), to deal with the problematic blue region (hue angles in the neighborhood of 275°)
- Compensation for neutral colors (the primed values in the $L^{*} C^{*} h^{*}$ differences)
- Compensation for lightness ($S_{L}$)
- Compensation for chroma ($S_{C}$)
- Compensation for hue ($S_{H}$)

$$
\Delta E_{00}^{*}=\sqrt{\left(\frac{\Delta L^{\prime}}{k_{L} S_{L}}\right)^{2}+\left(\frac{\Delta C^{\prime}}{k_{C} S_{C}}\right)^{2}+\left(\frac{\Delta H^{\prime}}{k_{H} S_{H}}\right)^{2}+R_{T} \frac{\Delta C^{\prime}}{k_{C} S_{C}} \frac{\Delta H^{\prime}}{k_{H} S_{H}}}
$$

**Note:** The formulae below should use degrees rather than radians; the issue is significant for $R_{T}$.

The $k_{L}, k_{C}$, and $k_{H}$ are usually unity.

$$
\begin{aligned}
&\Delta L^{\prime}=L_{2}^{*}-L_{1}^{*} \\
\\
&\bar{L}=\frac{L_{1}^{*}+L_{2}^{*}}{2} \quad \bar{C}=\frac{C_{1}^{*}+C_{2}^{*}}{2} \\
\\
&a_{1}^{\prime}=a_{1}^{*}+\frac{a_{1}^{*}}{2}\left(1-\sqrt{\frac{\bar{C}^{7}}{\bar{C}^{7}+25^{7}}}\right) \quad a_{2}^{\prime}=a_{2}^{*}+\frac{a_{2}^{*}}{2}\left(1-\sqrt{\frac{\bar{C}^{7}}{\bar{C}^{7}+25^{7}}}\right) \\
\\
&\bar{C}^{\prime}=\frac{C_{1}^{\prime}+C_{2}^{\prime}}{2} \quad and \quad \Delta C^{\prime}=C_{2}^{\prime}-C_{1}^{\prime} \quad where \quad C_{1}^{\prime}=\sqrt{a_{1}^{\prime 2}+b_{1}^{*^{2}}} \quad C_{2}^{\prime}=\sqrt{a_{2}^{\prime 2}+b_{2}^{*^{2}}} \\
\\
&h_{1}^{\prime}=\arctan2\left(b_{1}^{*}, a_{1}^{\prime}\right) \enspace \text {mod} \; 360^{\circ}, \quad h_{2}^{\prime}=\arctan2\left(b_{2}^{*}, a_{2}^{\prime}\right) \enspace \text {mod} \; 360^{\circ}
\end{aligned}
$$

**Note:** The inverse tangent $\left(\tan ^{-1}\right)$ can be computed using a common library routine $a \tan 2\left(b, a^{\prime}\right)$ which usually has a range from −π to π radians; color specifications are given in 0 to 360 degrees, so some adjustment is needed. The inverse tangent is indeterminate if both a′ and b are zero (which also means that the corresponding C′ is zero); in that case, set the hue angle to zero. See Sharma 2005, eqn. 7.

$$
\Delta h^{\prime}= \begin{cases}h_{2}^{\prime}-h_{1}^{\prime} & \left|h_{1}^{\prime}-h_{2}^{\prime}\right| \leq 180^{\circ} \\ h_{2}^{\prime}-h_{1}^{\prime}+360^{\circ} & \left|h_{1}^{\prime}-h_{2}^{\prime}\right|>180^{\circ}, h_{2}^{\prime} \leq h_{1}^{\prime} \\ h_{2}^{\prime}-h_{1}^{\prime}-360^{\circ} & \left|h_{1}^{\prime}-h_{2}^{\prime}\right|>180^{\circ}, h_{2}^{\prime}>h_{1}^{\prime}\end{cases}
$$

**Note:** When either $C_{1}^{\prime}$ or $C_{2}^{\prime}$ is zero, then $\Delta \mathrm{h}^{\prime}$ is irrelevant and may be set to zero. See Sharma 2005, eq. 10.

$$
\Delta H^{\prime}=2 \sqrt{C_{1}^{\prime} C_{2}^{\prime}} \sin \left(\Delta h^{\prime} / 2\right), \quad \bar{H}^{\prime}= \begin{cases}\left(h_{1}^{\prime}+h_{2}^{\prime}\right) / 2 & \left|h_{1}^{\prime}-h_{2}^{\prime}\right| \leq 180^{\circ} \\ \left(h_{1}^{\prime}+h_{2}^{\prime}+360^{\circ}\right) / 2 & \left|h_{1}^{\prime}-h_{2}^{\prime}\right|>180^{\circ}, h_{1}^{\prime}+h_{2}^{\prime}<360^{\circ} \\ \left(h_{1}^{\prime}+h_{2}^{\prime}-360^{\circ}\right) / 2 & \left|h_{1}^{\prime}-h_{2}^{\prime}\right|>180^{\circ}, h_{1}^{\prime}+h_{2}^{\prime} \geq 360^{\circ}\end{cases}
$$

**Note:** When either $C^{\prime}{ }_{1}$ or $C_{2}^{\prime}$ is zero, then $\mathrm{H}^{\prime}$ is $h_{1}^{\prime}+h_{2}^{\prime}$ (no divide by 2 ; essentially, if one angle is indeterminate, then use the other angle as the average; relies on indeterminate angle being set to zero). See Sharma 2005, eqn. 7 and p. 23 stating most implementations on the internet at the time had "an error in the computation of average hue".

$$
\begin{aligned}
&T=1-0.17 \cos \left(\bar{H}^{\prime}-30^{\circ}\right)+0.24 \cos \left(2 \bar{H}^{\prime}\right)+0.32 \cos \left(3 \bar{H}^{\prime}+6^{\circ}\right)-0.20 \cos \left(4 \bar{H}^{\prime}-63^{\circ}\right) \\
\\
&S_{L}=1+\frac{0.015(\bar{L}-50)^{2}}{\sqrt{20+(\bar{L}-50)^{2}}} \quad S_{C}=1+0.045 \bar{C}^{\prime} \quad S_{H}=1+0.015 \bar{C}^{\prime} T \\
\\
&R_{T}=-2 \sqrt{\frac{\bar{C}^{\prime 7}}{\bar{C}^{\prime 7}+25^{7}}} \sin \left[60^{\circ} \cdot \exp \left(-\left[\frac{\bar{H}^{\prime}-275^{\circ}}{25^{\circ}}\right]^{2}\right)\right]
\end{aligned}
$$

## CMC l:c (1984)

In 1984, the Colour Measurement Committee of the Society of Dyers and Colourists defined a difference measure, also based on the L*C*h color model. Named after the developing committee, their metric is called CMC l:c. The quasimetric has two parameters: lightness (l) and chroma (c), allowing the users to weight the difference based on the ratio of l:c that is deemed appropriate for the application. Commonly used values are 2:1[20] for acceptability and 1:1 for the threshold of imperceptibility.

The distance of a color ($L_{2}^{*},C_{2}^{*},h_{2})$ to a reference ($L_{1}^{*},C_{1}^{*},h_{1}$) is:

$$
\begin{aligned}
&\Delta E_{C M C}^{*}=\sqrt{\left(\frac{L_{2}^{*}-L_{1}^{*}}{l \times S_{L}}\right)^{2}+\left(\frac{C_{2}^{*}-C_{1}^{*}}{c \times S_{C}}\right)^{2}+\left(\frac{\Delta H_{a b}^{*}}{S_{H}}\right)^{2}} \\
\\
&S_{L}= \begin{cases}0.511 & L_{1}^{*}<16 \\
\frac{0.040975 L_{1}^{*}}{1+0.01765 L_{1}^{*}} & L_{1}^{*} \geq 16 \quad S_{C}=\frac{0.0638 C_{1}^{*}}{1+0.0131 C_{1}^{*}}+0.638 \quad S_{H}=S_{C}(F T+1-F)\end{cases} \\
\\
&F=\sqrt{\frac{C_{1}^{* 4}}{C_{1}^{* 4}+1900} \quad T= \begin{cases}0.56+\left|0.2 \cos \left(h_{1}+168^{\circ}\right)\right| & 164^{\circ} \leq h_{1} \leq 345^{\circ} \\
0.36+\left|0.4 \cos \left(h_{1}+35^{\circ}\right)\right| & \text { otherwise }\end{cases} }
\end{aligned}
$$
