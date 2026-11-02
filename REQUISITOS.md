# Compatibilidade — aplicativo 0.14.1 e preparador 1.3.0

| Item | Perfil suportado |
|---|---|
| Sistema | Windows 11 x64, Intel/AMD. |
| Processador | x64 com AVX2; 6 núcleos ou mais recomendados. |
| RAM | 32 GB ou mais. |
| GPU | NVIDIA CUDA com 12 GB de VRAM dedicada ou mais. |
| Unidade padrão | NTFS/exFAT, 32 GB ou maior e 25 GiB livres na preparação. |
| Unidade com Gemma opcional | NTFS/exFAT, 64 GB ou maior e 32 GiB livres na preparação. |
| Conexão da unidade | USB 3.0 recomendado; SSD externo reduz o tempo de carga. |
| Áudio | Microfone e saída para prática por voz. Kokoro e vozes pt-BR acompanham o aplicativo. |
| Rede | Preparação inicial, ativação e verificações periódicas da licença. |

FAT32 não comporta os modelos maiores que 4 GB. Execução somente em CPU,
Windows ARM e GPUs AMD/Intel **não são suportados**. VRAM dedicada não é a memória
compartilhada anunciada pelo Windows.

A preparação padrão baixa **12.937.222.832 bytes**. Incluir Gemma acrescenta
**5.154.941.280 bytes**, totalizando **18.092.164.112 bytes**.
O espaço livre inclui margem para extração e temporários. Documentos e relatórios
do usuário precisam de espaço adicional. GB é decimal; GiB é binário.

Qwen3.5 e Ornith continuam disponíveis. Gemma 4 E4B é opcional e experimental.
O contexto configurado é 32.768 tokens, com um modelo por vez; embeddings usam CPU.
Whisper Small/Base e Kokoro incluídos no aplicativo também executam na CPU.
A alternativa CPU dos iniciadores não representa suporte a equipamentos sem GPU.

Ativação não acompanha automaticamente a mídia externa para outro PC. A conta
admite uma instalação ativa e até duas horas offline, limitadas ao período válido.
Consulte as condições atualizadas no portal. A confirmação dos requisitos
não afasta os direitos legais do consumidor.
