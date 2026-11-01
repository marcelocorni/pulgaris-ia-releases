# Pulgaris — releases oficiais

Simulações, treinamento de comunicação e preparação oral com o conhecimento
do próprio usuário: **Academic, Interview, Oral e Present**.

Este repositório público recebe **instaladores, changelogs, instruções e
verificações SHA-256**. Os fontes do Pulgaris ficam em repositório privado.
A licença do aplicativo é comercial; dependências e modelos conservam suas
respectivas licenças, disponíveis nos pacotes.

**As novas edições estão em preparação.** Consulte os arquivos efetivamente
disponíveis na [página de releases](https://github.com/marcelocorni/pulgaris-ia-releases/releases).
Não há instaladores hospedados no portal.

## Antes de contratar

Leia [REQUISITOS.md](REQUISITOS.md) e confira seu computador. O perfil atual
exige Windows 11 x64, GPU NVIDIA CUDA com 12 GB de VRAM dedicada ou mais e
32 GB de RAM ou mais. Execução sem GPU, Windows ARM e GPUs AMD/Intel
não são suportados.

Para a IA em pen drive/HD: unidade NTFS/exFAT de **32 GB ou maior** e
**25 GiB livres** (aproximadamente 27 GB). **64 GB ou mais e USB 3.0 são
recomendados**. FAT32 não comporta os modelos maiores que 4 GB.

## Qual instalador escolher?

| Pacote | Finalidade |
|---|---|
| `Pulgaris-<versão>-Setup-win-x64.exe` | Instala o aplicativo Windows, o runtime .NET e o Whisper base local. |
| `Pulgaris-Preparador-<versão>-Setup-win-x64.exe` | Copia o preparador para uma nova pasta no pen drive ou HD. É pequeno; baixa os modelos e llama.cpp posteriormente. |
| `SHA256SUMS.txt` | Permite conferir a integridade dos arquivos da mesma release. |

Os dois assistentes são feitos em Inno Setup. Baixar um instalador não
substitui a contratação e a ativação do aplicativo.

## Instalar e ativar

1. Baixe os arquivos da release desejada e confira o changelog.
2. Verifique o SHA-256 com `Get-FileHash -Algorithm SHA256 'arquivo.exe'` e
   compare com `SHA256SUMS.txt` daquela release.
3. Instale o aplicativo e execute o preparador em uma **nova pasta vazia**
   da unidade escolhida. Nenhuma unidade é formatada.
4. Execute `Preparar-Pulgaris.cmd`. O mesmo fluxo baixa, verifica e prepara
   runtime e modelos. São **12.937.222.832 bytes (~12,94 GB)** de downloads.
5. Informe a pasta preparada nas configurações do aplicativo.
6. Ative com sua conta e licença do [portal Pulgaris](https://pulgaris.com.br).

Veja o [guia completo](INSTALACAO.md). Cada release informa suas versões,
mudanças, limitações e instruções específicas. Não reutilize hashes de
outra release.

## Modelos fixados

| Componente | Versão / quantização | Bytes |
|---|---|---:|
| Ornith | 1.5 9B Q4_K_M | 5.780.090.816 |
| Qwen | 3.5 9B Q4_K_M | 5.680.522.464 |
| Embeddings | Qwen3-Embedding 0.6B Q8_0 | 639.150.592 |
| Transcrição | Whisper base multilíngue GGML | 147.951.465 |
| Runtime de IA | llama.cpp b11853, CUDA 12.4 | Downloads fixados pelo preparador |

Somente um modelo é usado por vez. Ao terminar, use o respectivo controle
**Parar**. Os modelos não são iniciados automaticamente. A voz utiliza uma
voz pt-BR instalada no Windows; não há modelo ONNX próprio neste pacote.

## Licenciamento e privacidade

Uma instalação ativa por conta. Ativação e verificações periódicas exigem
internet. A licença permite até **2 horas offline**, limitadas à validade
do período contratado. Para trocar de computador, libere o vínculo na sua
conta. Documentos, gravações e respostas das simulações permanecem locais.

Feedback qualitativo: confira as referências. O aplicativo não atribui nota
oficial nem garante aprovação em avaliações, entrevistas ou apresentações.

Contato e condições comerciais: [pulgaris.com.br](https://pulgaris.com.br).
Não publique senhas, chaves de ativação, documentos ou dados de pagamento
em issues ou comentários deste repositório.
