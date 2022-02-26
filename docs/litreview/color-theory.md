---
title: 'Color Theory'
author: 'Matthew Furr'
date: '02/24/2022'
---

# {{ $frontmatter.title }} <Badge text="Copied" type="warning"/>

## Overview

## From TAGA

### Principles of Color

Before discussing and introducing color and tone reproduction, it is important to understand the phenomenon of color. This requires an examination and understanding of light. Light is radiation in the form of electromagnetic waves that can be perceived by the human eye. More specifically, the visible spectrum ranges from approximately 380nm to 730nm. (Ohta & Robertson, 2006)A uniform intensity of light across the visible spectrum is perceived as white light. However, when the uniform balance is disrupted, we perceive new colors. Sir Isaac Newton first demonstrated this principle in 1704.  (Field, 1999)Within the visible spectrum there are an infinite range of components with slight variations in wavelength, resulting in more colors than names can be given. Colored objects have certain reflectance characteristics—various wavelengths are reflected and absorbed resulting in the human eye perceiving the object as colored.  (Ohta & Robertson, 2006)

Color mixing systems are based on the basic characteristics of color stimulus. Known as a trichromatic system, colors can be matched by a mixture of three reference stimuli, typically red, green, and blue. Any three values used to describe colors, such as tristimulus values, are referred to as colorimetric values.  (Ohta & Robertson, 2006)

Color perception is a complex sensation that is influenced by the illuminant, physical properties of the object, and physiological characteristics of the observer. For this reason, the printing industry has established standards for both the light source and observer. The quality, or “color,” of the light used in graphic arts is defined as D50 or 5000K. This was chosen because it comes close to natural daylight. (CGATS.5) The Commission internationale de l'éclairage established the 2° standard observer in 1931 to represent an average human’s chromatic response within a 2° arc inside the fovea or central area of the retina. Tristimulus values vary depending on the field of view, therefore, the 2° arc is selected due to the distribution of rods and, more importantly, cones within the retina. The last variable influencing the perception of color is the substrate. Printers control the color printed through the selection of the substrate, the inks or pigments, and the process used to apply the ink. (Field, 1999)

## From O'Hara

When speaking of color and light in 1704, Sir Isaac Newton declared that “the rays to speak properly are not colored; in them there is nothing else than a certain power and disposition to stir up a sensation of this or that color” (Newton, 1704). The human eye is capable of perceiving energy with wavelengths between 380 and 730 nm, and we interpret that energy as light and color. When the intensity of light is uniform across the visible spectrum, we perceive white light, light that is balanced. When this balance is disrupted, we become conscious of color (Field, 1999). When light energy strikes an object, various wavelengths are either absorbed, transmitted, refracted or reflected. By  measuring the reflected light at discrete intervals or wavelengths, one can determine the spectral reflectance for that object.

For the perception of color to occur, there must be a light source, an object to reflect the light, and an observer (Billmeyer & Saltzman, 1981). Any light source, object, or observer has different properties that influence the perception of color. Light sources are differentiated by their color temperature. Objects are differentiated by their spectral reflectance, and observers by their sensitivities to blue, red or green light. If any of these ingredients change, the perceived color changes.

When specifying color, the printing industry has established standards for the light source and the observer in order to limit the variables for color perception. D50 lighting is the North American industry standard for color specification (CGATS.5). D50 lighting provides a balanced white light that simulates direct sunlight (Sharma, 2003). The Commission Internationale de TEclairage (CIE) established the 2° standard observer in 1931 that provides tristimulus values of blue, green and red sensitivities of the eye representative of normally sighted humans. With the light source and the observer standardized, the only variable affecting color perception is the press sheet itself. The printer controls the color of the printed product through the selection of substrate, ink pigments, and the application of ink to the substrate.

Process color inks carry transparent pigments that selectively absorb approximately one-third of the spectrum. Ideally, each ink would completely absorb one-third of the visible spectrum and fully transmit the remaining two-thirds; for example, magenta would completely remove green light and fully transmit blue and red light. However, our inks are imperfect filters—magenta absorbs most, but not all, green light, it absorbs some  of the red light and a considerable amount of blue light. The greatest amount of unwanted absorption is termed hue error, and the smallest amount of unwanted absorption is termed grayness (Preucil, 1957). These unwanted absorptions can be quantified through densitometric measurements, as established by Preucil, but the most accurate and descriptive way to assess color is through spectral data (Briies, May & Fuchs, 2000). Figure 2, Ideal vs. Actual Process Colors, shows the spectral reflectance curves of actual inks and theoretical, “ideal” inks.

```js chart-editor
// <block:data:0>
const data = {
  labels: ['380', '390', '400', '410', '420', '430', '440', '450', '460', '470', '480', '490', '500', '510', '520', '530', '540', '550', '560', '570', '580', '590', '600', '610', '620', '630', '640', '650', '660', '670', '680', '690', '700', '710', '720', '730'],
  datasets: [
    {
      label: 'D50',
      data: [17.92, 20.98, 23.91, 25.89, 24.45, 29.83, 49.25, 56.45, 59.97, 57.76, 74.77, 87.19, 90.56, 91.32, 95.07, 91.93, 95.70, 96.59, 97.11, 102.09, 100.75, 102.31, 100.00, 97.74, 98.92, 93.51, 97.71, 99.29, 99.07, 95.75, 98.90, 95.71, 98.24, 103.06, 99.19, 87.43, 91.66, 92.94, 76.89, 86.56, 92.63, 78.27, 57.72, 82.97, 78.31, 79.59, 73.44, 63.95, 70.81, 74.48],
      borderColor: Utils.CHART_COLORS.red,
      fill: true,
      backgroundColor: function(context) {
        const chart = context.chart;
        const {ctx, chartArea} = chart;

        if (!chartArea) {
          // This case happens on initial chart load
          return;
        }
        return getGradient(ctx, chartArea);
      },
    }
    // {
    //   label: 'D65',
    //   data: [39.90, 44.86, 46.59, 51.74, 49.92, 54.60, 82.69, 91.42, 93.37, 86.63, 104.81, 116.96, 117.76, 114.82, 115.89, 108.78, 109.33, 107.78, 104.78, 107.68, 104.40, 104.04, 100.00, 96.34, 95.79, 88.69, 90.02, 89.61, 87.71, 83.30, 83.72, 80.05, 80.24, 82.30, 78.31, 69.74, 71.63, 74.37, 61.62, 69.91, 75.11, 63.61, 46.43, 66.83, 63.40, 64.32, 59.47, 51.97, 57.46, 60.33],
    //   borderColor: Utils.CHART_COLORS.blue,
    //   backgroundColor: Utils.transparentize(Utils.CHART_COLORS.blue, 0.5),
    // }
  ]
};
// </block:data>

// <block:functions:2>
let width, height, gradient;
function getGradient(ctx, chartArea) {
  const chartWidth = chartArea.right - chartArea.left;
  const chartHeight = chartArea.bottom - chartArea.top;
  if (!gradient || width !== chartWidth || height !== chartHeight) {
    // Create the gradient because this is either the first render
    // or the size of the chart has changed
    width = chartWidth;
    height = chartHeight;
    gradient = ctx.createLinearGradient(chartArea.right, 0, chartArea.left, 0);
    gradient.addColorStop(0, 'rgba(65, 16, 8, 1.00)');
    gradient.addColorStop(0.2, 'rgba(214, 57, 51, 1.00)');
    gradient.addColorStop(0.4, 'rgba(207, 181, 26, 1.00)');
    gradient.addColorStop(0.6, 'rgba(118, 170, 28, 1.00)');
    gradient.addColorStop(0.8, 'rgba(49, 125, 182, 1.00)');
    gradient.addColorStop(1, 'rgba(35, 43, 69, 1.00)');
  }

  return gradient;
}

const title = (tooltipItems) => {
  console.log(tooltipItems);
  let title = '';
  tooltipItems.forEach(function(tooltipItem) {
    title += tooltipItem.label;
  });
  return title + 'nm';
};
// </block:functions>

// <block:config:1>
const config = {
  type: 'line',
  data: data,
  options: {
    responsive: true,
    plugins: {
      legend: {
        position: 'top',
      },
      tooltip: {
        position: 'nearest',
        mode: 'index',
        callbacks: {
          // footer: function(context) {
          //   return context.parsed.y + ' cm';
          // },
          title: title,
          // footer: function(tooltipItems, data) {
          //   // console.log(data);
          //   console.log(tooltipItems);
          //   var label = myChart.data.labels[tooltipItems.dataIndex];
          //   // var value = config.data.datasets[tooltipItem.datasetIndex].data[tooltipItem.index];
          //   return label + 'nm yo';
          // },
        },
      },
      title: {
        display: true,
        text: 'Daylight Sources'
      }
    },
    scales: {
      y: {
        min: 0,
        //max: 50,
      }
    }
  },
};
// </block:config>

module.exports = {
  config: config,
};
```

Process color printing is a subtractive process in which color filters are applied in the form of cyan, magenta and yellow inks to selectively remove the red, green and blue light, respectively, that is reflected from the substrate. Due to their transparent qualities, the three subtractive primaries can be printed in combinations to create a wide range of colors. The range of colors that a particular printing system or device can create is the color gamut of that system (Sharma, 2004).

The color gamut of printed media is established by the substrate, the CMYK solids and their overprints. Color gamuts are commonly represented by three-dimensional color models such as CIELAB or CIELCH. These color spaces have lightness as the vertical axis, with dark at the lower end (a value of 0) and light on top (a value of 100). The vertical axis itself is achromatic, representing perfect neutrals ranging from black to white. Moving perpendicularly away from the lightness axis in any direction introduces color. Hues are arranged around the vertical axis in a perimeter in which 0° is red, 90° is yellow, 180° is green and 270° is blue. Moving away from the axis in any direction introduces color that increases in chroma with distance from the neutral axis. Thus, of the three attributes of color, any hue is possible, but the gamut is bounded by lightness and chroma.

In a printing system, the lightest point of the gamut is the substrate itself. Each substrate has its own reflective qualities, but process color printing works best on a substrate that is as bright and white as possible. That is to say that the substrate should reflect as much light as possible and reflect the light evenly across the visible spectrum so as to be without color cast (Field, 1999). The darkest point of the gamut is the point of greatest density possible with the ink set.

The chroma boundaries of the printing system are determined by the density and the purity of the process colors CMY. The more effectively each ink selectively removes one-third of the spectrum, the further from the neutral axis the solid is extended. Two color overprints of CM, MY, and CY extend the gamut into the blue, red and green areas, respectively. These create the “top shell” of the color gamut and establish the chroma boundaries, as can be seen in Figure 3, Two-Color Overprints. Beyond the purity and density of the primary colors, the gamut is also affected by ink film trapping.

As three- and four-color overprints are introduced, the resulting colors lose saturation and lightness and fill in the color gamut beneath the two-color “top shell” until the greatest density the inks can achieve is reached at the base of the color gamut, as illustrated in Figure 4, Three- and Four-Color Overprints.

While chroma is a function of purity as well as density, the purity issues of hue error and grayness can be disregarded for the following discussion. For a given set of process inks, the hue error and grayness of the inks are inherent in their pigments, so the only variable the pressman controls is the density, as determined by ink film thickness. Density is also a matter of pigment load, and great strides have been made in dispersing more concentrated amounts of pigment with finer grinds to allow thinner ink films, but again, for a given set of inks, the pigment load is established also, leaving the issue of gamut boundary to density through ink film thickness. Generally speaking, the greater the ink film thickness, the greater the density. However, while the chroma boundaries are set  by density, the color gamut is more than the outlying points of the boundaries, it also includes the points within the boundaries. The more points present, the greater number of potential colors that exist within the gamut. Thus for each printer, the ink film thickness must be optimized to yield the greatest range of tone reproduction.
