# REGRAS UTILIZADAS PARA O CÁLCULO DA PLANILHA DE QUANTIFICAÇÃO #

## Backbone óptico SECUNDÁRIO
    # SEQ #
    Quantidade de cabo necessária: (Medida básica para cálculo dos lances de cabo backbone) x 1,2;
    Tipo cabo:
    Quantidade de Pigtail 1,5m com conector LC Duplo: (quantidade total de backbones nos demais pavimentos) * (quantidade de fibras por cabo) / 2
    Quantidade de Acoplador óptico LC Duplo: mesma quantidade de Pigtail 1,5m com conector LC Duplo
    Quantidade de DIO 24 portas: ceil((Quantidade de Pigtail 1,5m com conector LC Duplo)%24)
    Quantidade de cordão óptico 3m simples: (quantidade de Pigtail 1,5m com conector LC Duplo) * 2

    # SET #
    Terminador óptico: quantidade total de backbones nos demais pavimentos
    Pigtail 3m com conector LC Duplo: (quantidade total de backbones nos demais pavimentos) * (quantidade de fibras por cabo) / 2



    # Backbone óptico DA SEQ tem que ter:
    - fibra ( tamanho, tipo, característica)
    - DIO
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
    - bandeja fixa: //
    - patch cable 2,5m azul (dados) : [porcentagem_dados * quantidade_pontos_de_rede]
    - patch cable 2,5m vermelho (camera): [porcentagem_de_CFTV * quantidade_pontos_de_rede]
    - patch cable 2,5m amarelo (voz): [porcentagem_de_VOIP * quantidade_pontos_de_rede]
    - rack fechado de largura 19" + tamanho: //
    - exaustor 19": //

    # MISCELANEA
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
    - Régua de fechamento - 1U
    - Porca Gaiola - pacote com 10 unidades