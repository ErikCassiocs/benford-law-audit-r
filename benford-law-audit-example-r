set.seed(123)
n <- 5000

dados <- data.frame(
  ID = 1:n,
  Tipo = sample(c("Receita","Despesa","Pagamento","Imposto"), n, replace = TRUE),
  Valor = round(rlnorm(n, meanlog = 8, sdlog = 1), 2)
)
View(dados)

indices_fraude <- sample(1:n, 200)

dados$Valor[indices_fraude] <- sample(
  seq(8000, 9999, 1),
  length(indices_fraude),
  replace = TRUE
)

dados$Primeiro_Digito <- sapply(dados$Valor, function(x) {
  as.numeric(substr(as.character(abs(x)), 1, 1))
})

freq_obs <- table(dados$Primeiro_Digito)
freq_obs <- freq_obs / sum(freq_obs)

freq_esp <- sapply(1:9, function(d) log10(1 + 1/d))

freq_obs <- freq_obs[as.character(1:9)]
freq_obs[is.na(freq_obs)] <- 0

barplot(freq_obs, col = "lightblue", ylim = c(0, 0.35))
lines(1:9, freq_esp, type = "b", pch = 19, lwd = 2)

obs <- as.numeric(freq_obs * n)
teste <- chisq.test(obs, p = freq_esp)
print(teste)

#Chi-squared test for given probabilities


X-squared = 78.34, df = 8, p-value = 1.054e-13

suspeitos <- subset(dados, Primeiro_Digito %in% c(8,9))
head(suspeitos)
