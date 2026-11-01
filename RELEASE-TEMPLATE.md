# Pulgaris <versão> — <data>

## Mudanças

- <Mudança concreta observável nesta versão.>
- <Correção e seu efeito.>

## Arquivos

| Arquivo | Versão | SHA-256 |
|---|---|---|
| Pulgaris-<versão>-Setup-win-x64.exe | <versão> | <hash real> |
| Pulgaris-Preparador-<versão>-Setup-win-x64.exe | <versão do preparador> | <hash real> |

Os dois instaladores usam Inno Setup. Compare os hashes com o arquivo
SHA256SUMS.txt anexado a esta release. Nenhum fonte do aplicativo é incluído.
O arquivo release.json acompanha os dois instaladores para atualizar os
links de download direto do portal após a publicação dos assets.

## Instalação / atualização

<Informar passos específicos da versão e preservação dos dados.>
<Indicar se o kit de IA pode ser mantido ou exige nova pasta.>

Consulte INSTALACAO.md e REQUISITOS.md anexos. Uma instalação ativa por
conta; internet para ativação e confirmações periódicas; até 2 horas offline
limitadas ao período contratado.

## Componentes congelados

Qwen3.5 9B Q4_K_M; Ornith 1.5 9B Q4_K_M; Qwen3-Embedding 0.6B Q8_0;
Whisper base multilíngue; llama.cpp b11853 CUDA 12.4. Preparação inicial:
12,94 GB de downloads; unidade de 32 GB ou maior com 25 GiB livres em
NTFS/exFAT. Recomendado: 64 GB e USB 3.0. Atualizar este bloco se houver
nova homologação de manifesto.

## Verificação e limitações

<Registrar testes realmente realizados, perfil de hardware e pendências.>
<Não confundir compilação com execução manual ou homologação de hardware.>
