# Teste de vozes ANGEL — Google Colab gratuito

**Status:** execução real concluída no runtime gratuito do Colab. Python 3.12 isolado, Kokoro instalado, pipeline PT-BR inicializado, três WAVs gerados e ZIP não vazio verificado. A avaliação artística das vozes ainda está pendente; nenhuma voz foi aprovada.

## Abrir o notebook

1. Abra o notebook no Google Colab pelo link abaixo.
2. Se o Google pedir login, entre na sua conta Google.
3. Use o ambiente padrão gratuito. Não escolha Colab Pro, não aceite upgrade e não informe pagamento.
4. Execute as células na ordem, começando pela instalação.
5. Ouça os WAVs e baixe o ZIP gerado na última célula.
6. Envie aqui o ZIP ou os áudios para avaliarmos pronúncia, naturalidade, interpretação e consistência.

Notebook: https://colab.research.google.com/github/walysonfelipenascimento-gif/anegel-anime/blob/main/production/audio/kokoro-colab-ptbr.ipynb

## O que foi preparado

- O erro observado nas capturas foi confirmado: o PyPI declara `kokoro 0.9.4` compatível com Python `>=3.10,<3.13`; o runtime do Colab mostrado na sessão não atende a esse limite.
- O notebook cria um Python 3.12 isolado usando `uv`, instala o Kokoro nesse ambiente e executa a inicialização e os testes chamando explicitamente esse interpretador.
- Kokoro com o pipeline de idioma `p`, indicado pelo README oficial para português brasileiro.
- As três vozes documentadas para PT-BR são `pf_dora`, `pm_alex` e `pm_santa`; o notebook tenta gerar uma amostra de cada uma e registra falhas individuais.
- A célula de exportação reúne os WAVs produzidos em um ZIP.

## Limitações e cuidados

- A execução real confirmou instalação, importação, inicialização PT-BR e geração dos três WAVs no runtime gratuito.
- O ZIP `ANGEL_testes_de_voz_Kokoro.zip` foi criado e verificado como não vazio, contendo os três WAVs.
- A qualidade artística, a naturalidade e a adequação das vozes aos personagens continuam **não avaliadas**; geração técnica não significa aprovação.
- O Colab gratuito tem limites de uso e pode desconectar sessões.
- Não usa chave de API nem serviço de créditos pagos, mas o acesso gratuito ao Colab não é garantido sem limites.
- Não selecionar plano pago, trial, upgrade ou inserir cartão.
- Antes de uso público/comercial do anime, revisar separadamente a licença vigente do código, pesos do modelo e arquivos de voz. Não presumir que uma licença cobre todos os componentes.
- Nenhuma voz foi definida como voz oficial do elenco ANGEL.
