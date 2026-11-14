# ANGEL — progresso do teste Kokoro no Google Colab

**Data:** 2026-11-13  
**Status:** síntese de amostras concluída; avaliação artística das vozes ainda pendente.

## Objetivo permanente de áudio

A meta de ANGEL não é apenas obter uma voz que leia o texto. Queremos vozes em português brasileiro com qualidade alta e interpretação expressiva, naturais e consistentes entre cenas e episódios. A voz deve conseguir transmitir emoções com nuance — calma, sabedoria, gentileza, humor, curiosidade, preocupação, tensão, mistério, alegria, tristeza e intensidade — sem soar mecânica ou exagerada.

Critérios obrigatórios de avaliação:
- pronúncia e naturalidade em português brasileiro;
- ritmo, pausas, respiração, entonação e dicção;
- variedade emocional e capacidade de interpretação;
- consistência da identidade vocal entre diferentes falas;
- clareza, qualidade técnica e possibilidade de exportar áudio;
- licença compatível com o uso e eventual distribuição da obra;
- fluxo gratuito, sem assinatura, compra de créditos, cartão ou teste pago.

Nenhuma voz está aprovada para um personagem até ser ouvida e avaliada. As vozes testadas são candidatas técnicas, não decisões de elenco.

## Conexão e ambiente

- O perfil de navegador foi conectado à conta Google do usuário para acessar o Colab.
- O notebook foi aberto a partir deste repositório: `production/audio/kokoro-colab-ptbr.ipynb`.
- Foi conectado o runtime padrão gratuito do Google Colab. Não foi selecionado Colab Pro, GPU paga ou cobrança.
- O runtime padrão apresentou Python 3.13.18, incompatível com Kokoro 0.9.4.
- A primeira célula criou um ambiente Python 3.12 isolado em `/content/angel-kokoro-venv/`.
- Kokoro `>=0.9.4`, `soundfile` e `espeak-ng` foram instalados.
- A verificação real de importação passou: `Kokoro importado no Python 3.12 com sucesso`.
- O pipeline de português brasileiro `KPipeline(lang_code='p')` inicializou com sucesso.

## Síntese de teste confirmada

A célula de comparação foi executada no Colab e gerou três WAVs:
- `pf_dora.wav` — aproximadamente 281.29 KB
- `pm_alex.wav` — aproximadamente 287.15 KB
- `pm_santa.wav` — aproximadamente 287.15 KB

Local temporário no runtime:
`/content/angel_voice_tests/`

O arquivo ZIP `ANGEL_testes_de_voz_Kokoro.zip` foi criado e verificado como não vazio, com tamanho aproximado de 855.91 KB. A validação sequencial confirmou os três arquivos WAV e o ZIP.

Avisos observados durante a execução:
- aviso de repositório padrão do modelo Kokoro;
- aviso de requisições não autenticadas ao Hugging Face Hub;
- avisos internos do PyTorch sobre dropout e depreciação de weight_norm.
Nenhum desses avisos impediu a geração dos três arquivos.

## O que está comprovado e o que falta

**Comprovado tecnicamente:** ambiente gratuito preparado, Kokoro instalado, pipeline PT-BR inicializado, três amostras WAV geradas e ZIP não vazio criado.

**Ainda não comprovado:** naturalidade percebida, qualidade artística, emoção, adequação a Angel/Nara/Iren/adversário, estabilidade de interpretação entre cenas, licença final para distribuição e persistência dos arquivos fora da sessão temporária do Colab.

A execução e a geração dos arquivos não equivalem a aprovação das vozes. É necessário ouvir e comparar as três amostras antes de qualquer escolha.

## Próximas etapas

1. Garantir que o ZIP seja baixado e guardado fora do armazenamento temporário do Colab.
2. Ouvir e comparar as três amostras em português brasileiro.
3. Avaliar interpretação emocional, naturalidade, dicção, ritmo e consistência.
4. Se Kokoro não atingir a qualidade artística desejada, pesquisar e testar outras alternativas realmente gratuitas, sem créditos pagos, assinaturas, cartão ou trials.
5. Só então decidir se alguma voz serve como base para testes de elenco. Não atribuir automaticamente Dora, Alex ou Santa a Angel, Nara, Iren ou outros personagens.
6. Criar amostras específicas para as falas e intenções vocais aprovadas no guia de leitura do Episódio 1.

## Separação de projetos

Todo este trabalho pertence exclusivamente ao anime ANGEL e ao repositório `walysonfelipenascimento-gif/anegel-anime`. Não alterar Nexora, Brasil Regencial ou seus serviços e bancos de dados.
