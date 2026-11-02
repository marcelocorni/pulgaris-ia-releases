# Pulgaris 0.13.3 + preparador 1.3.0 — 02/11/2026

Aplicativo e preparador Windows x64, com os dois instaladores Inno Setup.
Qwen3.5 permanece padrão, Ornith é mantido e Gemma 4 E4B entra como opção experimental.

## O que mudou desde a última distribuição pública

- Modo simples por padrão, importação com indexação automática e configurações de áudio salvas.
- Simulador prepara as N perguntas em conjunto, apresenta uma por vez e guarda o roteiro
  para retomada. Avançar por perguntas preparadas não abre o gerador novamente.
- Avaliação imediata ou ao final, com resposta de referência e fontes. **Avaliar respostas
  salvas** permite terminar com o que foi respondido se faltarem perguntas válidas.
- **Perguntar à IA** responde a perguntas do usuário sobre o documento, com citações.
- Whisper Small e Base multilíngues incluídos. Revisão textual opcional da transcrição,
  com original preservado e aplicação explícita da sugestão.
- Kokoro local com Dora, Alex e Santa, leitura automática de perguntas, velocidade,
  pausas e dicionário de pronúncia. Vozes do Windows não são necessárias.
- Atalhos configuráveis, restritos à janela em foco. Correção do salvar e avançar no modo
  de avaliação ao final e preservação das respostas quando a geração seguinte falha.
- **Gemma 4 E4B (experimental)** no aplicativo e download opcional no preparador 1.3.0.
  Seus iniciadores experimentais anteriores são compatíveis. Granite permanece de fora.

## Arquivos e integridade

| Arquivo | Tamanho | SHA256 |
|---|---:|---|
| Pulgaris-0.13.3-Setup-win-x64.exe | 999.885.636 bytes | 0311f381578c8a50e2ef8eeb856548156bdc7c38d0716376fc8bdb9a9c6b780b |
| Pulgaris-Preparador-1.3.0-Setup-win-x64.exe | 3.057.430 bytes | 4aaae1bbdd31aea136b0057eec729170a2ddc861847f3087a069203c2b4ba024 |

Confira SHA256SUMS.txt da mesma release. Os EXEs são os pacotes aprovados para publicação,
preservados sem recompilação. Os fontes permanecem no repositório privado.
release.json acompanha os instaladores para atualizar os links diretos do portal.

## Instalar / atualizar / ativar

1. Feche o Pulgaris e instale o aplicativo sobre a versão atual. Biblioteca, histórico,
   configurações e ativação são preservados.
2. Para uma nova unidade, use o preparador em uma nova pasta e execute
   **Preparar-Pulgaris.cmd**. Responda **S** para Gemma experimental ou **N** para manter
   o conjunto padrão. O mesmo fluxo baixa e confere todos os componentes.
3. Selecione a pasta preparada no aplicativo e ative com sua conta e período válido.
4. Importe o documento, aguarde a indexação e inicie a simulação. Para testar Gemma,
   ative Modo avançado e selecione a opção marcada experimental.
5. Deixe os modelos iniciados manualmente parados antes das operações do aplicativo.
   Use um modelo por vez e seu controle Parar ao encerrar os testes.

Consulte INSTALACAO.md e REQUISITOS.md. Uma instalação ativa por conta; internet para
ativação e verificações periódicas; até duas horas offline, limitadas ao período válido.
Uma mídia externa não transfere automaticamente a ativação para outro computador.

## Componentes congelados e hardware

- Qwen3.5 9B Q4_K_M, Ornith 1.5 9B Q4_K_M e Qwen3-Embedding 0.6B Q8_0.
- Gemma opcional: 4 E4B IT QAT Q4_0, revisão 4b4a2c1d584be7264f87aac328a1bc739ce81b6c.
- llama.cpp b11853 CUDA 12.4; contexto 32k; um modelo por vez.
- Whisper Small/Base e Kokoro 82M v1.0 FP32, com três vozes pt-BR, incluídos no aplicativo.
- Downloads do preparador: 12,94 GB no conjunto padrão; 18,09 GB com Gemma.
- Windows 11 x64, AVX2, 32 GB de RAM e NVIDIA com 12 GB de VRAM dedicada ou mais.
- Unidade NTFS/exFAT: padrão de 32 GB ou maior com 25 GiB livres; com Gemma,
  64 GB ou maior com 32 GiB livres. USB 3.0 recomendado; FAT32 não é suportado.

MODELOS-FIXADOS.json e os avisos de terceiros acompanham a release. Não há atualização
automática para pesos latest.

## Verificações e limites

290 testes automatizados aprovados; 432 arquivos do pacote conferidos, com SQLite,
FTS5, Kokoro e Whisper. Os testes da interface foram executados em ambiente virtual,
sem controlar janelas nativas. Testes reais de roteiro com Qwen, Ornith e Gemma,
um modelo por vez, confirmaram apresentação individual e avanço pelo roteiro salvo.
Todos os serviços iniciados nesses testes foram encerrados.

Gemma permanece experimental. Referências existentes e perguntas aceitas pelo validador
não garantem todas as interpretações da IA. Materiais curtos podem não sustentar a
quantidade solicitada; as perguntas e respostas válidas são preservadas.
A avaliação é qualitativa e não equivale à nota de uma banca nem garante aprovação.
Os instaladores ainda não possuem assinatura digital comercial.

Portal, conta e suporte: https://pulgaris.com.br


---

# Pulgaris 0.10.2 — 01/11/2026

## Correções

- Importação com pasta de IA vazia apresenta orientação em português antes de ler o documento.
- A Biblioteca permite escolher a pasta do ambiente de IA e salvá-la sem mudar de tela.
- Preferências também oferece seleção de pasta, evitando digitar o caminho manualmente.
- O carregador de embeddings valida a configuração antes de converter ou acessar o caminho.

## Como atualizar e importar

1. Encerre o aplicativo e instale Pulgaris-0.10.2-Setup-win-x64.exe.
2. Na Biblioteca, clique em Escolher pasta e selecione a pasta do ambiente de IA
   que contém models, llama.cpp e os iniciadores. Clique em Salvar pasta.
3. Encerre modelos e embeddings que tenham sido iniciados manualmente.
4. Com a conta ativada e o período de acesso válido, importe seu PDF.

O aplicativo administra o início e o encerramento dos embeddings durante a
indexação. PDFs digitalizados sem texto extraível exigem OCR; consulte os
avisos apresentados após a extração. Os documentos são processados localmente.

O preparador correspondente é Pulgaris-Preparador-1.2.0-Setup-win-x64.exe.
Para uma nova instalação de IA, prepare uma pasta vazia com o preparador.
O ambiente existente pode continuar sendo selecionado nas configurações.
Consulte INSTALACAO.md, REQUISITOS.md e SHA256SUMS.txt anexos.

## Componentes fixados e requisitos

Qwen3.5 9B Q4_K_M, Ornith 1.5 9B Q4_K_M, Qwen3-Embedding 0.6B Q8_0,
llama.cpp b11853 CUDA 12.4 e Whisper base multilíngue homologado.
Windows 11 x64, 32 GB de RAM e GPU NVIDIA CUDA com 12 GB de VRAM dedicada.
A preparação inicial baixa aproximadamente 12,94 GB e exige unidade
NTFS/exFAT de pelo menos 32 GB com 25 GiB livres. Recomendado: 64 GB e USB 3.0.

## Validação

63 testes de biblioteca, configuração, interface, respostas e treinamento
aprovados, incluindo a reprodução de pasta vazia e verificação de que nenhum
modelo é iniciado nem índice publicado nesse caso. Serviços de IA simulados;
o HD de desenvolvimento não foi alterado e não foram executados modelos reais.