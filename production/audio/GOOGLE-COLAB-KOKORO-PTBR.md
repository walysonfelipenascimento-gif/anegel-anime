# Teste de vozes ANGEL — Google Colab gratuito

**Status:** notebook corrigido para contornar a incompatibilidade do Python padrão do Colab; a nova instalação ainda precisa ser testada. Nenhum áudio foi gerado e nenhuma voz foi aprovada.

## Abrir o notebook

1. Abra o notebook no Google Colab pelo link abaixo.
2. Se o Google pedir login, entre na sua conta Google.
3. Use o ambiente padrão gratuito. Não escolha Colab Pro, não aceite upgrade e não informe pagamento.
4. Execute as células na ordem, começando pela instalação.
5. Ouça os WAVs e baixe o ZIP gerado na última célula.
6. Envie aqui o ZIP ou os áudios para avaliarmos pronúncia, naturalidade, interpretação e consistência.

Notebook: https://colab.research.google.com/github/walysonfelipenascimento-gif/anegel-anime/blob/main/production/audio/kokoro-colab-ptbr.ipynb

## O que foi preparado

- Python 3.12 isolado dentro da sessão Colab, pois o ambiente padrão pode usar uma versão de Python incompatível com o Kokoro 0.9.4.
- Kokoro com o pipeline de idioma `p`, indicado no README oficial para português brasileiro.
- As células de inicialização e geração chamam explicitamente o Python 3.12 isolado; não dependem do Python padrão do notebook.
- Teste protegido das vozes candidatas `pf_dora`, `pm_alex` e `pm_santa`; cada uma pode falhar dependendo da versão/arquivos disponíveis.
- Amostra comum para comparação.
- Exportação WAV e ZIP.

## Limitações e cuidados

- O notebook ainda não foi executado com a correção em uma sessão Colab; portanto instalação, disponibilidade de vozes e qualidade permanecem **não verificadas**.
- O Colab gratuito tem limites de uso e pode desconectar sessões.
- Não usa chave de API nem serviço de créditos pagos, mas o acesso gratuito ao Colab não é garantido sem limites.
- Não selecionar plano pago, trial, upgrade ou inserir cartão.
- Antes de uso público/comercial do anime, revisar separadamente a licença vigente do código, pesos do modelo e arquivos de voz. Não presumir que uma licença cobre todos os componentes.
- Nenhuma voz foi definida como voz oficial do elenco ANGEL.
