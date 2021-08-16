
<!-- README.md is generated from README.Rmd. Please edit that file -->

# American Policing

<!-- badges: start -->
<!-- badges: end -->

The goal of the American Policing Project is to demonstrate the
inefficacy and infefficiency of the American policing system.

An example visualization below:

``` r
ggplot(police_race, aes(fct_reorder(factor(race), percent), percent, fill = factor(race))) +
  geom_col() +
  scale_y_continuous(labels = scales::percent_format(scale = 1), limits = c(0, 100), breaks = c(0, 25, 50, 75, 100)) +
  coord_flip() +
  labs(title = "Police Murders per State by Race", x = "", y = "", fill = "Race") +
  theme_premium() +
  facet_geo( ~ name) +
  scale_fill_premium() +
  guides(fill = guide_legend(nrow = 1)) +
  theme(plot.title = element_text(hjust = 0.5, size = 18),
        legend.position = "bottom",
        axis.text.x = element_text(size = 8),
        axis.text.y = element_text(size = 8),
        panel.spacing = unit(0.1, "lines"),
        strip.text = element_text(face = "bold", family = "Fira Sans", hjust = 0.5, size = 14))
ggsave(here::here("Images/map_violence.png"), height = 10, width = 18)
```

![](Images/map_violence.png)

An example table as well:

<div style="text-align:center">

<div id="jrxeqoiyoo" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>@import url("https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
html {
  font-family: 'Open Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#jrxeqoiyoo .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 5px;
  border-top-color: #000000;
  border-right-style: solid;
  border-right-width: 3px;
  border-right-color: #000000;
  border-bottom-style: solid;
  border-bottom-width: 5px;
  border-bottom-color: #000000;
  border-left-style: solid;
  border-left-width: 3px;
  border-left-color: #000000;
}

#jrxeqoiyoo .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#jrxeqoiyoo .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#jrxeqoiyoo .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#jrxeqoiyoo .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#jrxeqoiyoo .gt_col_headings {
  border-top-style: solid;
  border-top-width: 4px;
  border-top-color: #000000;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#jrxeqoiyoo .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 80%;
  font-weight: bold;
  text-transform: uppercase;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#jrxeqoiyoo .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 80%;
  font-weight: bold;
  text-transform: uppercase;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#jrxeqoiyoo .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#jrxeqoiyoo .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#jrxeqoiyoo .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#jrxeqoiyoo .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 80%;
  font-weight: bolder;
  text-transform: uppercase;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#jrxeqoiyoo .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 80%;
  font-weight: bolder;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#jrxeqoiyoo .gt_from_md > :first-child {
  margin-top: 0;
}

#jrxeqoiyoo .gt_from_md > :last-child {
  margin-bottom: 0;
}

#jrxeqoiyoo .gt_row {
  padding-top: 3px;
  padding-bottom: 3px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#jrxeqoiyoo .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 80%;
  font-weight: bolder;
  text-transform: uppercase;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#jrxeqoiyoo .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#jrxeqoiyoo .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#jrxeqoiyoo .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#jrxeqoiyoo .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#jrxeqoiyoo .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#jrxeqoiyoo .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#jrxeqoiyoo .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#jrxeqoiyoo .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#jrxeqoiyoo .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 0px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 0px;
  border-right-color: #D3D3D3;
}

#jrxeqoiyoo .gt_sourcenote {
  font-size: 12px;
  padding: 10px;
}

#jrxeqoiyoo .gt_left {
  text-align: left;
}

#jrxeqoiyoo .gt_center {
  text-align: center;
}

#jrxeqoiyoo .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#jrxeqoiyoo .gt_font_normal {
  font-weight: normal;
}

#jrxeqoiyoo .gt_font_bold {
  font-weight: bold;
}

#jrxeqoiyoo .gt_font_italic {
  font-style: italic;
}

#jrxeqoiyoo .gt_super {
  font-size: 65%;
}

#jrxeqoiyoo .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table">
  <thead class="gt_header">
    <tr>
      <th colspan="3" class="gt_heading gt_title gt_font_normal gt_bottom_border" style="font-family: &#39;Fira Sans&#39;; font-size: x-large; text-align: center; font-weight: bold;">Percent of Murders per Race</th>
    </tr>
    
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1">Race</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1">N</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1">Percent</th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_center" style="font-size: medium; text-align: center;">White</td>
<td class="gt_row gt_center" style="font-size: medium; text-align: center;">4083</td>
<td class="gt_row gt_center" style="background-color: #B71C1C; color: #FFFFFF; font-size: medium; text-align: center;">43.33&percnt;</td></tr>
    <tr><td class="gt_row gt_center" style="font-size: medium; text-align: center;">Black</td>
<td class="gt_row gt_center" style="font-size: medium; text-align: center;">2353</td>
<td class="gt_row gt_center" style="background-color: #F24236; color: #FFFFFF; font-size: medium; text-align: center;">24.97&percnt;</td></tr>
    <tr><td class="gt_row gt_center" style="font-size: medium; text-align: center;">Hispanic</td>
<td class="gt_row gt_center" style="font-size: medium; text-align: center;">1677</td>
<td class="gt_row gt_center" style="background-color: #EC605D; color: #000000; font-size: medium; text-align: center;">17.80&percnt;</td></tr>
    <tr><td class="gt_row gt_center" style="font-size: medium; text-align: center;">Unknown race</td>
<td class="gt_row gt_center" style="font-size: medium; text-align: center;">987</td>
<td class="gt_row gt_center" style="background-color: #EE9797; color: #000000; font-size: medium; text-align: center;">10.48&percnt;</td></tr>
    <tr><td class="gt_row gt_center" style="font-size: medium; text-align: center;">Asian</td>
<td class="gt_row gt_center" style="font-size: medium; text-align: center;">138</td>
<td class="gt_row gt_center" style="background-color: #FFE5E9; color: #000000; font-size: medium; text-align: center;">1.46&percnt;</td></tr>
    <tr><td class="gt_row gt_center" style="font-size: medium; text-align: center;">Native American</td>
<td class="gt_row gt_center" style="font-size: medium; text-align: center;">131</td>
<td class="gt_row gt_center" style="background-color: #FFE6E9; color: #000000; font-size: medium; text-align: center;">1.39&percnt;</td></tr>
    <tr><td class="gt_row gt_center" style="font-size: medium; text-align: center;">Pacific Islander</td>
<td class="gt_row gt_center" style="font-size: medium; text-align: center;">53</td>
<td class="gt_row gt_center" style="background-color: #FFEBEE; color: #000000; font-size: medium; text-align: center;">0.56&percnt;</td></tr>
  </tbody>
  
  
</table>
</div>

</div>

In that case, don’t forget to commit and push the resulting figure
files, so they display on GitHub.
