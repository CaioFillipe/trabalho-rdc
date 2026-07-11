# REGRAS UTILIZADAS PARA O CÁLCULO DA PLANILHA DE QUANTIFICAÇÃO #

## Backbone óptico PRIMÁRIO
    #Backbone primário tem que ter:
    - Terminador óptico [caso o cabo tenha <= 12 fibras] ou DIO 
    [ > 12 fibras]
    - Pigtail LC Duplo 
    - Cabo de fibra óptico

    #REGRAS PARA ESPECIFICAÇÃO DAS QUANTIDADES:
    - Pigtail LC DUPLO (3m) = [quantidade_de_fibras] / 2
    - Tipo/modelo/caracteristicas de cabo de fibra: especificado_na_entrada
    - Caso seja terminador óptico -> terminador óptico 12 portas: 1 unidade
    - Caso seja DIO -> Dio 24 portas 19'' 1U: ceil((Quantidade de Pigtail (3m)  com conector LC Duplo)/24)


## Backbone óptico SECUNDÁRIO
    # SEQ #
    Medida básica para cálculo dos lances de cabo backbone:
        - Caso seja linear: distância entre os backbones
        - Caso seja vertical: Considere n o número de pavimentos, e p o tamanho do pé direito, a distância básica é:
        [(n+1)(n+2)/2] * p - (2 * p)
    Quantidade de cabo necessária: (Medida básica para cálculo dos lances de cabo backbone) x 1,2 [ se for vertical] ou x 1,1 [ se for linear]
    Tipo/modelo/caracteristicas de cabo de fibra: especificado_na_entrada
    Quantidade de Pigtail 1,5m com conector LC Duplo: (quantidade total de backbones nos demais pavimentos) * (quantidade de fibras por cabo) / 2
    Quantidade de Acoplador óptico LC Duplo: mesma quantidade de Pigtail 1m com conector LC Duplo
    Quantidade de DIO 24 portas: ceil((Quantidade de Pigtail 1,5m com conector LC Duplo)/24)
    Quantidade de cordão óptico 3m simples: (quantidade de Pigtail 1m com conector LC Duplo) * 2

    # SET #
    Terminador óptico: quantidade total de backbones nos demais pavimentos
    Pigtail 3m com conector LC Duplo: (quantidade total de backbones nos demais pavimentos) * (quantidade de fibras por cabo) / 2



    # Backbone óptico DA SEQ tem que ter:
    - fibra ( tamanho [em metros], tipo [loose ou tight buffer], especificação[OM1, OM2, OS2...], característica[FOMMIG,  ou FOSM])
    - DIO[caso haja mais de 12 fibras] ou Terminador óptico se for menos de 12 fibras
    - acoplador óptico
    - pigtail 1,5m
    - cordão óptico 3m
    
    # Backbone óptico DA SET tem que ter:
    - terminador óptico 
    - pigtail 3m


## MALHA HORIZONTAL ##

    # MATERIAIS DE CABEAMENTO (cálculo de quantificação):
    - cabo utp : [metragem_malha_horizontal] * [pontos_de_rede]
    - tomada rj45: [pontos_de_rede]
    - espelho 4x4 - 2 furações: [pontos_de_telecom]
    - patch cord azul 3m: [quantidade_pontos_de_rede - quantidade_de_CFTV]
    - patch cord branco 1m: [quantidade_de_CFTV]
    - patch panel: ceil([quantidade_pontos_de_rede]/24)
    - organizador: 2 * [quantidade_patch_panel]
    - bandeja fixa: [quantidade_de_exaustor]
    - patch cable 2,5m azul (dados) : [porcentagem_dados * quantidade_pontos_de_rede]
    - patch cable 2,5m vermelho (camera): [porcentagem_de_CFTV * quantidade_pontos_de_rede]
    - patch cable 2,5m amarelo (voz): [porcentagem_de_VOIP * quantidade_pontos_de_rede]
    - rack (fechado ou aberto) de largura 19" e tamanho: (quantidade_patch_panel*2  + quantidade_de_organizador_de_cabos + quantidade_de_exaustor) * 1,5 -> Observação: se o tamanho do rack superar 48U, divida em um rack de 48U e o outro com o tamanho restante da operação
    - exaustor 19" [somente se o rack for fechado] : [quantidade_de_rack]

    # MISCELANEA (ELEMENTOS ACESSÓRIOS)
    - Etiquetas de identficação da porta do Patch Panel: [24 * quantidade_patch_panel]
    - Etiquetas de identficação Patch Cable: [quantidade_pontos_rede * 2]
    - Etiquetas de identficação do Patch Panel: [quantidade_patch_panel]
    - Etiquetas de identificação Tomadas e Espelhos: [quantidade_espelhos + quantidade_tomadas] 
    - Etiquetas de identificação Cabos UTP - MH: [quantidade_pontos_rede * 2]
    - Abraçadeiras plásticas, pacote 100 unidades
    - Abraçadeiras de velcro, rolo 3 m
    - Régua com 8 tomadas - filtro de linha
    - Régua de fechamento - 1U: [tamanho_rack - espaco_ocupado]
    - Porca Gaiola - pacote com 10 unidades: ceil([4 * unidade_ocupada_por_equipamentos]/10)

    # MATERIAIS DE CABEAMENTO DE REDE tem que ter:
        - cabo utp
        - tomada rj45
        - espelho 4x4 - 2 furações
        - patch cord azul 3m
        - patch cord branco 1m
        - patch panel
        - organizador
        - bandeja fixa
        - patch cable 2,5m azul (dados)
        - patch cable 2,5m vermelho (camera)
        - patch cable 2,5m amarelo (voz)
        - rack fechado de largura 19" + tamanho
        - exaustor 19" 

        #MISCELANEA
        - Etiquetas de identficação da porta do Patch Panel
        - Etiquetas de identficação Patch Cable
        - Etiquetas de identficação do Patch Panel
        - Etiquetas de identificação Tomadas e Espelhos
        - Etiquetas de identificação Cabos UTP - MH
        - Abraçadeiras plásticas, pacote 100 unidades
        - Abraçadeiras de velcro, rolo 3 m
        - Régua com 8 tomadas - filtro de linha
        - Porca Gaiola - pacote com 10 unidades

# ENTRADAS BACKBONE ÓPTICO #
    - Número de pavimentos da edificação
        -> caso seja mais de um, especificar o tamanho do pé direito
    - Número de pares de fibras que ficarão disponíveis
    - Especificação do cabo de fibra óptica (FOMMIG, FOSM)
    - Característica da fibra óptica; (OM1, OM2, OM3, OM4..., OS1, OS2.... Tight Buffer ou Loose)
    - Quantidade de backbones por andar
    - Verificação da existência de backbone primário e/ou secundário (Apenas backbone primário - ligação entre prédios, apenas backbone primário - sem conexão externa, apenas backbone secundário, backbone primário e secundário)
    
# ENTRADAS MALHA HORIZONTAL #
    - Número de pavimentos da edificação
    - Número de pontos por pavimento (telecom ou rede)
    - Medida básica para cálculo da distância da MH
    - Especificação de categoria do cabo de MH
    - Quantidade de pontos de telecom/redes total, destacando o atendimento do serviço que será atendido (com porcentagem de pontos de rede, pontos de VOIP, ou cftv)

# REGRAS BÁSICAS PARA O CABO:" #
    1. Um par de fibra óptica sempre possui 2 fibras
    2. Um ponto de telecom significa dois pontos de rede
    3. Caso haja mais de um backbone por pavimento, multiplicar a quantidade dos elementos da quantificação do backbone óptico pela quantidade de backbones por pavimento
    4. Os tamanhos dos racks são vendidos de: de 0U a 12U, 2 a 2, se for de 12U a 48U, é de 4 em 4 U.
