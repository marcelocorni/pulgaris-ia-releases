# Pulgaris 0.10.1 — 01/11/2026

Plataforma Windows para simulações, treinamento de comunicação e preparação oral
com documentos do próprio usuário: Academic, Interview, Oral e Present.

## Mudanças

- Cards do início com dimensões iguais, espaçamento uniforme e proporções mais compactas.
- Biblioteca local com indexação, respostas fundamentadas e citações dos documentos.
- Reconhecimento de fala local e leitura na saída de áudio selecionada.
- Ativação vinculada à instalação, renovação, expiração e confirmação offline limitada.
- Aplicativo 0.10.1 e preparador 1.2.0 em instaladores Inno Setup com a identidade Pulgaris.

## Instalação e atualização

1. Confira REQUISITOS.md e os hashes em SHA256SUMS.txt.
2. Encerre o aplicativo e execute Pulgaris-0.10.1-Setup-win-x64.exe.
3. Para preparar uma nova pasta em pen drive/HD, use Pulgaris-Preparador-1.2.0-Setup-win-x64.exe.
4. Configure a pasta de IA no aplicativo e ative sua conta em Conta e ativação.

O preparador baixa versões fixadas de Qwen3.5 9B Q4_K_M, Ornith 1.5 9B Q4_K_M,
Qwen3-Embedding 0.6B Q8_0 e llama.cpp b11853 CUDA 12.4. A preparação inicial
baixa aproximadamente 12,94 GB. Use unidade NTFS/exFAT de pelo menos 32 GB,
com 25 GiB livres; recomenda-se 64 GB e USB 3.0.

O aplicativo inclui Whisper base multilíngue congelado para transcrição local.
O perfil suportado exige Windows 11 x64, 32 GB de RAM e GPU NVIDIA CUDA
com pelo menos 12 GB de VRAM dedicada. Consulte as instruções completas anexas.

## Conta e licença

Crie a conta em https://pulgaris.com.br e faça a ativação dentro do aplicativo.
Uma instalação ativa por conta. As confirmações são renovadas periodicamente;
o uso offline fica limitado a duas horas desde a última confirmação válida e
ao período contratado. Para trocar de computador, libere o vínculo em Minha conta.
Uma licença válida também é necessária para importar e indexar documentos.

## Validação

Nove testes da interface e cinco renderizações de tamanhos/temas passaram na
correção dos cards. O pacote Windows teve os arquivos, o runtime e o Whisper
conferidos. O portal passou por 185 testes locais, incluindo MariaDB isolado.
Os testes locais de pagamento e checkout usaram respostas simuladas; a
conferência de pagamentos reais cabe aos testes na integração publicada.

O software oferece avaliação qualitativa para treinamento. Revise as respostas
e as referências aos documentos. As licenças de terceiros acompanham os pacotes.