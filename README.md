# ANA-505-Week-4-Activity
ANA 505 Week 4 Activity exercise

#Week 4: dplyr package



data_color <- data.frame(HairEyeColor)



head(data_color,10)



install.packages("dplyr")
library(dplyr)



select(data_color, Hair, Sex)



select_hairsex <- select(data_color, Hair = Hair, Sex = Sex)



select_hairsex <- select(select_hairsex, -Sex)



rename(data_color, Gender = Sex)



data_color[,"Gender"] <- NA
data_color



filter_male <- filter(data_color, Sex == "Male")
filter_male <- select(filter_male, Sex)
filter_male



group_by(data_color, Sex)

#After you run it, write the total here:592

total=mutate(data_color, total=cumsum(Freq))
total



filter_female <- filter(data_color, Sex == "Female")
filter_female <- select(filter_female, Sex)
filter_female



bind_rows(filter_male,filter_female)


#Here we are using 'arrange' function to arrange a dataframe with 'Eye' Column

arrange_data_color_by_Eye<- arrange(data_color, desc(Eye))
arrange_data_color_by_Eye

