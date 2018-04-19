reg Violence_count  ///
 Nightlight_mean RoadDensity_mean Diamond InfantMortality_mean Mineral Petroleum Population_mean_ipolate area
 
xtset objectid Year


xtreg Violence_count  ///
 Nightlight_mean RoadDensity_mean Diamond InfantMortality_mean Mineral Petroleum Population_mean_ipolate area, fe
 
 
xtreg Violence_count  ///
 Nightlight_mean RoadDensity_mean Diamond InfantMortality_mean Mineral Petroleum Population_mean_ipolate area, re
 

xttest0


xtreg Violence_count  ///
 Nightlight_mean RoadDensity_mean Diamond InfantMortality_mean Mineral Petroleum Population_mean_ipolate area, fe

estimates store fixed
 
xtreg Violence_count  ///
 Nightlight_mean RoadDensity_mean Diamond InfantMortality_mean Mineral Petroleum Population_mean_ipolate area, re
 
estimates store random

hausman fixed random
