3) Quais campos apresentam menor correlação com o campo “phishing”?

Código usado:

SELECT phishing, AVG(url_length) AS media_url_length, AVG(n_dots) AS media_n_dots, AVG(n_hypens) AS media_n_hypens, AVG(n_slash) AS media_n_slash, AVG(n_questionmark) AS media_n_questionmark, AVG(n_equal) AS media_n_equal, AVG(n_at) AS media_n_at, AVG(n_redirection) AS media_n_redirection FROM phishing_data GROUP BY phishing;

As variáveis com menor diferença foram:

- n_dots
- n_redirection

Essas variáveis apresentaram valores médios muito próximos entre URLs legítimas e phishing, indicando baixa capacidade de distinção entre os dois grupos
