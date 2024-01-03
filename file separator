import os
import shutil
import glob

# Caminho da pasta original
pasta_origem = r"C:\Users\LSVictorHugo\Desktop\ArquivosXML\Alpargatas XMLs1\Alpargatas XMLs"

# Número máximo de arquivos por pasta
arquivos_por_pasta = 220

# Lista de arquivos XML na pasta original
arquivos_xml = glob.glob(os.path.join(pasta_origem, '*.xml'))

# Pasta de destino base
pasta_destino_base = r"C:\Users\LSVictorHugo\Downloads\CTE EMISSAO"

# Função para dividir arquivos
def dividir_arquivos(arquivos, tamanho, pasta_destino_base):
    for i in range(0, len(arquivos), tamanho):
        pasta_destino = os.path.join(pasta_destino_base, f'pasta_{i // tamanho + 1}')

        # Criar a pasta de destino se ela não existir
        if not os.path.exists(pasta_destino):
            os.makedirs(pasta_destino)

        # Mover os arquivos para a pasta de destino
        for arquivo in arquivos[i:i + tamanho]:
            shutil.move(arquivo, pasta_destino)

# Chamar a função para dividir os arquivos
dividir_arquivos(arquivos_xml, arquivos_por_pasta, pasta_destino_base)

print("Divisão concluída.")
