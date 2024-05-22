
library(gridExtra)

ct <- read.csv("./data/ct_2010_I.csv")
ruca <- read.csv("./data/ruca2010revised2.csv")
ruca$Primary.RUCA.Code.2010 <- as.factor(ruca$Primary.RUCA.Code.2010)

names(ruca)[names(ruca) == 'GEOID5'] <- 'ID'

ct2 <- merge(ruca, ct, by="ID")
#ct2$Primary.RUCA.Code.2010 <- as.factor(ct2$Primary.RUCA.Code.2010)

# library(ggplot2)
# ggplot(data = ct2, aes(x = f1, y = x)) + 
#   geom_boxplot(aes(fill = f2), width = 0.8) + theme_bw()


library(reshape2)
ct_Male_age = melt(ct2, id.vars = c("Primary.RUCA.Code.2010", "ID"), measure.vars = c("MALE0C10","MALE5C10","MALE10C10","MALE15C10","MALE20C10","MALE25C10","MALE30C10","MALE35C10","MALE40C10","MALE45C10","MALE50C10","MALE55C10","MALE60C10","MALE65C10","MALE70C10","MALE75C10","MALE80C10","MALE85C10"))

library(ggplot2)
male_plot <- ggplot(ct_Male_age,aes(x=Primary.RUCA.Code.2010,y=value))+geom_boxplot(aes(fill=variable), outlier.shape =  NA) + 
ylim(0, 600)


library(reshape2)
ct_Female_age = melt(ct2, id.vars = c("Primary.RUCA.Code.2010", "ID"), measure.vars = c("FEM0C10","FEM5C10","FEM10C10","FEM15C10","FEM20C10","FEM25C10","FEM30C10","FEM35C10","FEM40C10","FEM45C10","FEM50C10","FEM55C10","FEM60C10","FEM65C10","FEM70C10","FEM75C10","FEM80C10","FEM85C10"))

library(ggplot2)
female_plot <- ggplot(ct_Female_age,aes(x=Primary.RUCA.Code.2010,y=value))+geom_boxplot(aes(fill=variable), outlier.shape =  NA) + 
  ylim(0, 600)

grid.arrange(male_plot, female_plot, nrow = 2, ncol = 1)



library(reshape2)
ct_Race_age = melt(ct2, id.vars = c("Primary.RUCA.Code.2010", "ID"), measure.vars = c("WHITE10","BLACK10","AMERIND10","ASIAN10","PACIFIC10","OTHRACE10"))

library(ggplot2)
race_plot <- ggplot(ct_Race_age,aes(x=Primary.RUCA.Code.2010,y=value))+geom_boxplot(aes(fill=variable), outlier.shape =  NA) + 
  ylim(0, 600)


library(reshape2)
ct_hispanic_age = melt(ct2, id.vars = c("Primary.RUCA.Code.2010", "ID"), measure.vars = c("HSP0C10","HSP5C10","HSP10C10","HSP15C10","HSP20C10","HSP25C10","HSP30C10","HSP35C10","HSP40C10","HSP45C10","HSP50C10","HSP55C10","HSP60C10","HSP65C10","HSP70C10","HSP75C10","HSP80C10","HSP85C10"
))

library(ggplot2)
hispanic_plot <- ggplot(ct_hispanic_age,aes(x=Primary.RUCA.Code.2010,y=value))+geom_boxplot(aes(fill=variable), outlier.shape =  NA) + 
  ylim(0, 600)

grid.arrange(hispanic_plot, race_plot, nrow = 2, ncol = 1)







library(reshape2)
ct_own_age = melt(ct2, id.vars = c("Primary.RUCA.Code.2010", "ID"), measure.vars = c("OWN1PERS10","OWN2PERS10","OWN3PERS10","OWN4PERS10","OWN5PERS10","OWN6PERS10","OWN7PERS10"))

library(ggplot2)
own_plot <- ggplot(ct_own_age,aes(x=Primary.RUCA.Code.2010,y=value))+geom_boxplot(aes(fill=variable), outlier.shape =  NA) + 
  ylim(0, 600)


library(reshape2)
ct_rent_age = melt(ct2, id.vars = c("Primary.RUCA.Code.2010", "ID"), measure.vars = c("RNT1PERS10","RNT2PERS10","RNT3PERS10","RNT4PERS10","RNT5PERS10","RNT6PERS10","RNT7PERS10"))

library(ggplot2)
rent_plot <- ggplot(ct_rent_age,aes(x=Primary.RUCA.Code.2010,y=value))+geom_boxplot(aes(fill=variable), outlier.shape =  NA) + 
  ylim(0, 600)

grid.arrange(own_plot, rent_plot, nrow = 2, ncol = 1)




library(reshape2)
ct_own_housing_age = melt(ct2, id.vars = c("Primary.RUCA.Code.2010", "ID"), measure.vars = c("OOHHR15C10","OOHHR25C10","OOHHR35C10","OOHHR45C10","OOHHR55C10","OOHHR65C10","OOHHR75C10","OOHHR85C10"))

library(ggplot2)
own_housing_plot <- ggplot(ct_own_housing_age,aes(x=Primary.RUCA.Code.2010,y=value))+geom_boxplot(aes(fill=variable), outlier.shape =  NA) + 
  ylim(0, 600)


library(reshape2)
ct_rent_housing_age = melt(ct2, id.vars = c("Primary.RUCA.Code.2010", "ID"), measure.vars = c("ROHHR15C10","ROHHR25C10","ROHHR35C10","ROHHR45C10","ROHHR55C10","ROHHR65C10","ROHHR75C10","ROHHR85C10"))

library(ggplot2)
rent_housing_plot <- ggplot(ct_rent_housing_age,aes(x=Primary.RUCA.Code.2010,y=value))+geom_boxplot(aes(fill=variable), outlier.shape =  NA) + 
  ylim(0, 600)


grid.arrange(own_housing_plot, rent_housing_plot, nrow = 2, ncol = 1)











library(ggplot2)
library(gridExtra)
ggplot(ct2,aes(x=Primary.RUCA.Code.2010,y=FEMALES10))+geom_boxplot()


