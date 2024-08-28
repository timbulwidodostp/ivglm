# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Instrumental variable estimation of the causal exposure effect in generalized linear models Use ivglm With (In) R Software
install.packages("ivtools")
install.packages("instruments")
install.packages("arm")
library("ivtools")
library("instruments")
library("arm")
ivglm = read.csv("https://raw.githubusercontent.com/timbulwidodostp/ivglm/main/ivglm/ivglm.csv",sep = ";")
# Estimation Instrumental variable estimation of the causal exposure effect in generalized linear models Use ivglm With (In) R Software
glm_1 <- glm(formula=X~Z, data=ivglm)
glm_2 <- glm(formula=Y~X+L+X*L, data=ivglm)
ivglm <- ivglm(estmethod="ts", fitX.LZ=glm_1, fitY.LX=glm_2, data=ivglm, ctrl=TRUE) 
summary(ivglm)
# Instrumental variable estimation of the causal exposure effect in generalized linear models Use ivglm With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished