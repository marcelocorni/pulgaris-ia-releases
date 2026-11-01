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