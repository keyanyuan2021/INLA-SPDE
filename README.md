# INLA-SPDE
已知监测点发病率估计未监测点发病率，未考虑时间趋势，仅为贝叶斯空间模型
#相关性分析
#建立单变量模型，用于评估自变量和因变量间是否有相关关系（p<0.05）
#利用offset函数
mod1<-glm.nb(incident_cases ~ offset(log(population))+x1,data=data1)
summary(mod1)
