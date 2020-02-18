# Aula 1
install.packages("dplyr")
library(dplyr)

# 
select(iris)

# Mostra o BD
glimpse(iris)

# Mostra as Colunas Selecionadas
select(iris, Petal.Length, Petal.Width)

# Mostra as Linhas
filter(iris, Petal.Length > 2)

# %>% 
iris %>% 
  filter(Petal.Length > 2) %>% 
  select(Species)

# Altera os valores da tabela
mutate(iris, Petal.Length = Petal.Length + 2)

iris %>% 
  filter(Petal.Length > 2) %>% 
  mutate(Petal = Petal.Length + 2) %>% 
  select(Species, Petal) %>% 
  glimpse()

#Transmute é mutate + select unidos
t <- iris %>% 
      transmute(Petal = Petal.Length + 2, Species)

#
iris %>% 
  group_by(Species) %>% 
  summarise(media = mean(Petal.Length))
