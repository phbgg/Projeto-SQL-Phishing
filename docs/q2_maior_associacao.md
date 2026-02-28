2) Quais campos apresentam maior associação com o campo phishing (se a URL é phishing ou não)?


Código usado:

SELECT 
    phishing,
    AVG(url_length) AS media_url_length,
    AVG(n_dots) AS media_n_dots,
    AVG(n_hypens) AS media_n_hypens,
    AVG(n_slash) AS media_n_slash,
    AVG(n_questionmark) AS media_n_questionmark,
    AVG(n_equal) AS media_n_equal,
    AVG(n_at) AS media_n_at,
    AVG(n_redirection) AS media_n_redirection
FROM phishing_data
GROUP BY phishing;


Resultado:

<img width="1017" height="312" alt="Image" src="https://github.com/user-attachments/assets/e6a5b0ab-1ac2-48af-9b7b-e909809387aa" />

Podemos analisar que as variáveis com maior diferença da média são:

- url_length: Uma diferença de aproximadamente 43 caracteres entre as médias.
- n_slash: Uma diferença de aproximadamente 2.4 ocorrências entre as médias.
- n_equal: Também apresenta aumento relevante entre as médias.
- n_hypens: Indica maior presença de hífens em URLs phishing.

Assim podemos associar mais as variáveis url_length, n_slash, n_equal e n_hypens com a variável phishing.
