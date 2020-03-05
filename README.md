# Jiajia_Li
weather1<-mean(bike_df$humidity[which(bike_df$weather==1)],na.rm=TRUE)
weather2<-mean(bike_df$humidity[which(bike_df$weather==2)],na.rm=TRUE)
weather3<-mean(bike_df$humidity[which(bike_df$weather==3)],na.rm=TRUE)
weather4<-mean(bike_df$humidity[which(bike_df$weather==4)],na.rm=TRUE)
bike_df$humidity2<-bike_df$humidity
bike_df$humidity2[which(is.na(bike_df$humidity)&bike_df$weather==1)]<-weather1
bike_df$humidity2[which(is.na(bike_df$humidity)&bike_df$weather==2)]<-weather2
bike_df$humidity2[which(is.na(bike_df$humidity)&bike_df$weather==3)]<-weather3
bike_df$humidity2[which(is.na(bike_df$humidity)&bike_df$weather==4)]<-weather4
