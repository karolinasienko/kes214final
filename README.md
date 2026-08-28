# Time Series of Hurricane's Effect on Stream Water Concentrations

Author: [Karolina Sienko](https://github.com/karolinasienko)

Contributors: [Max Czapanskiy](https://github.com/FlukeAndFeather) & [Alessandra Vidal Meza](https://github.com/avidalmeza)

## Background
This repository contains all of the data and code used to analyze the effects of Hurricane Hugo's disturbance on stream water concentrations of potassium (K), nitrate (NO$_3$), magnesium (Mg), calcium, (Ca) and ammonium (NH$_4$), in the Puente Roto Mameyes (PRM) and Bisley Quebradas 1, 2 and 3 (BQ1, BQ2, BQ3) watersheds of the Luquillo Experimental Forest, Puerto Rico. The purpose is to reproduce Figure 3 (see below) from a paper done by Schaefer, Douglas. A. et al. titled *Effects of hurricane disturbance on stream water concentrations and fluxes in eight tropical forest watersheds of the Luquillo Experimental Forest, Puerto Rico* [(2000)](https://doi.org/10.1017/s0266467400001358).

![](../docs/eds214_paper_graph)


## Repository Contents

This repository contains multiple folders and files necessary for completing the analysis.

The [`docs`](docs/) folder contains the .html file used to create a webpage in GitHub Pages, as well as .png files of the original graph I replicated and my resulting graph.

The [`output`](output/) folder contains one .csv file, [`clean_fig3_long.csv`](output/clean_fig3_long.csv), that contains the 9-week moving average concentrations for each nutrient in each watershed.

The [`paper`](paper/) folder contains a Quarto markdown file that contains all of the analysis and resulting figure.

The [`R`](R/) folder contains [`moving-average.R`](R/moving-average.R) which is a file that defines the `moving_average()` function.

The [`raw_data`](raw_data/) folder contains all the raw data downloaded from EDI Data Portal. There is a .csv file for each of the three BQ watersheds and for the PRM watershed.

The [`scratch`](scratch/) folder contains [`spaghetti.R`](scratch/spaghetti.R) which has code from early analysis.

The [`1_clean_data.R`](1_clean_data.R) file contains the code for the clean data found in the [`output`](output/) folder.



## Data

The following data files for this analysis were downloaded from [EDI Data Portal](https://portal.edirepository.org/nis/mapbrowse?packageid=knb-lter-luq.20.4923064) and can be found in the folder `raw_data`:

- QuebradaCuenca1-Bisley.csv
- QuebradaCuenca2-Bisley.csv
- QuebradaCuenca3-Bisley.csv
- RioMameyesPuenteRoto.csv

Each .csv file was read in and filtered to the date range from October 18th, 1988 to December 31st, 1994. The relevant columns corresponding to Sample ID, Sample Date, and concentrations for K, NO$_3$, Mg, Ca, and NH$_4$ were also selected. 


## Results

The below graph shows the concentrations of Ca, K, Mg, NH$_4$, and NO$_3$ in the BQ1, BQ2, BQ3, and PRM watersheds in Bisley, Puerto Rico. The vertical line indicates the time of Hurricane Hugo's disturbance on September 19th, 1989.

![](../docs/fig3.png)


## References
McDowell, William H., and USDA Forest Service. International Institute Of Tropical Forestry (IITF). 2024. “Chemistry of Stream Water from the Luquillo Mountains.” [Environmental Data Initiative](https://doi.org/10.6073/PASTA/F31349BEBDC304F758718F4798D25458).

Schaefer, Douglas. A., William H. McDowell, Fredrick N. Scatena, and Clyde E. Asbury. 2000. “Effects of Hurricane Disturbance on Stream Water Concentrations and Fluxes in Eight Tropical Forest Watersheds of the Luquillo Experimental Forest, Puerto Rico.” [Journal of Tropical Ecology 16 (2): 189–207](https://doi.org/10.1017/s0266467400001358).