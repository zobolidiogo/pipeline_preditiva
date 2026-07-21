# Dicionário de Dados: `manutencao_preditiva.csv`

**Linhas:** 10.000
**Colunas:** 14
**Granularidade:** 1 linha = 1 produto/peça processada por um equipamento industrial

| Coluna | Tipo | Descrição | Valores / Faixa | Nulos |
|---|---|---|---|---|
| `udi` | int | Identificador único sequencial do registro (Unique Data Index) | 1 a 10000 | 0 |
| `id_produto` | string | Código do produto, prefixo indica a qualidade/tipo (L, M, H) | ex: `L47181`, `M14860`, `H29424` | 0 |
| `tipo` | categórica | Categoria de qualidade do produto | `L` (baixa), `M` (média), `H` (alta) | 0 |
| `temperatura_ar_k` | float | Temperatura do ar ambiente durante o processo | ~295.3 a 304.5 (Kelvin) | 500 |
| `temperatura_processo_k` | float | Temperatura do processo de usinagem | ~305.7 a 313.8 (Kelvin) | 500 |
| `velocidade_rotacao_rpm` | float | Velocidade de rotação da ferramenta | ~1168 a 2886 (rpm) | 500 |
| `torque_nm` | float | Torque aplicado durante o processo | ~3.8 a 76.6 (N·m) | 500 |
| `desgaste_ferramenta_min` | int | Tempo de uso/desgaste da ferramenta | 0 a 253 (min) | 0 |
| `falha_maquina` | binária | Variável-alvo geral: indica se houve falha da máquina | 0 = sem falha, 1 = falha | 0 |
| `falha_twf` | binária | Falha por desgaste da ferramenta (*Tool Wear Failure*) | 0 / 1 | 0 |
| `falha_hdf` | binária | Falha por dissipação de calor (*Heat Dissipation Failure*) | 0 / 1 | 0 |
| `falha_pwf` | binária | Falha de potência (*Power Failure*) | 0 / 1 | 0 |
| `falha_osf` | binária | Falha por sobrecarga (*Overstrain Failure*) | 0 / 1 | 0 |
| `falha_rnf` | binária | Falha aleatória, sem causa identificável (*Random Failure*) | 0 / 1 | 0 |