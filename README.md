# Compressão de Imagens via Transformada de Wavelet (JPEG 2000)

## Requisitos

```bash
pip install -r requirements.txt
```

## Configuração

1. Copie o arquivo `.env.example` para `.env`:

   ```bash
   cp .env.example .env
   ```

2. Edite o arquivo `.env` com o caminho da imagem que será usada na demonstração final de compressão.

## Uso

Todo o desenvolvimento está no notebook `wavelets.ipynb`, basta abri-lo e executar as células em ordem:

```bash
jupyter notebook wavelets.ipynb
```

O notebook segue o seguinte fluxo:

1. A ideia da transformada de Wavelet, começando com a wavelet de Haar em sinais 1D
2. A interpretação da transformada como uma mudança de base (Álgebra Linear)
3. A decomposição multinível e a extensão para imagens (2D)
4. Compressão de imagens via limiarização dos coeficientes
5. A wavelet CDF 9/7 do JPEG 2000 e o esquema *lifting*
6. Um pipeline de compressão simplificado no estilo JPEG 2000

> **Nota:** As imagens usadas no desenvolvimento vêm do próprio `scikit-image`, apenas a demonstração final usa a imagem configurada no `.env`.
