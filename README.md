# Tech-Challenge---IA-para-Devs---Fase-2

# Otimização de Alocação de Sensores de Segurança com Algoritmos Genéticos

## Introdução

Este projeto tem como objetivo otimizar a alocação de sensores de monitoramento em uma infraestrutura de TI. Através do uso de algoritmos genéticos, ele busca maximizar a segurança, focando nas áreas mais críticas e vulneráveis. O sistema equilibra a criticidade, probabilidade de ataque, custo e capacidade, garantindo um uso eficiente dos recursos disponíveis para monitoramento.

## Objetivos do Projeto
- Criticidade das Áreas: Avaliação baseada em fatores de vulnerabilidade.
- Probabilidade de Ataque: Análise de probabilidade para cada área monitorada.
- Restrições de Custo e Capacidade: Limites predefinidos para garantir a otimização dos recursos.

## Objetivos Específicos
- **Eficiência de Monitoramento**: Maximizar a alocação de sensores em áreas críticas com recursos limitados.
- **Minimização de Riscos**: Reduzir vulnerabilidades em áreas suscetíveis a ataques.
- **Comparação de Eficiência**: Avaliar a eficácia do algoritmo genético em comparação com métodos tradicionais, como Força Bruta e Método Guloso.

## Estrutura Técnica
- Sensores: 10 sensores disponíveis para alocação.
- Áreas Monitoradas: 5 áreas, cada uma com níveis variados de criticidade e vulnerabilidade.
- Critérios Avaliados:

    - Níveis de Criticidade (1 a 5)
    - Probabilidade de Ataque (0,01 a 0,5)
    - Custos de Implementação (R$ 100 a R$ 1.000)
    - Capacidade das Áreas (50 a 200 unidades)
    - Pontuações CVSS (0 a 10) para representar criticidade.

- Limites Operacionais:

- Custo Máximo Permitido: R$ 2.500
- Capacidade Máxima Permitida: 400 unidades

## Componentes do Código
- **Criptografia de Credenciais**: Utilização da biblioteca Fernet para armazenamento seguro de credenciais.
- **Avaliação de Vulnerabilidades (CVSS)**: Priorização das áreas com base nas pontuações de vulnerabilidade.
- **Geração de Relatórios**: Criação automática de relatórios em Excel, detalhando alocações, criticidades e custos.
- **Monitoramento de Criticidade**: Armazenamento de histórico e envio de alertas em casos críticos.

## Metodologia: Algoritmo Genético

### Fases do Algoritmo
1. *Inicialização*: Geração da população inicial com configurações de alocação de sensores.
2. *Função de Fitness*: 
- Avaliação de criticidade, probabilidade de ataque e pontuação CVSS.
- Penalização para soluções que ultrapassam limites de custo ou capacidade.
3. *Operadores Genéticos*:
- Cruzamento: Combina características das melhores soluções.
- Mutação: Introduz variações para explorar novas possibilidades.
- Seleção: Prioriza indivíduos com maior valor de fitness.
4. *Finalização*: Seleção da solução mais eficiente após várias gerações.

### Comparação com Métodos Convencionais
- **Força Bruta**: Garante a solução ótima, mas é computacionalmente caro.
- **Método Guloso**: Rápido, mas menos preciso comparado ao algoritmo genético.

## Resultados e Comparações
- **Melhor Alocação Identificada**:
 > Criticidade Total: 8,5
 > Custo Total: R$ 2.300
 > Capacidade Total: 370 unidades

## Comparação de Eficiência

Método	Fitness Máximo	Custo Total	Tempo de Execução (s)
Algoritmo Genético	8,5	R$ 2.300,00	2,3
Força Bruta	8,5	R$ 2.300,00	45
Método Guloso	7,2	R$ 1.950,00	0,8

| Método | Fitness Máximo | Custo Total | Tempo de Execução (s) |
| ------ | ------ | ------ | ------ | 
| Algoritmo Genético | 8,5 | R$ 2.300,00 | 2,3 |
| Força Bruta | 8,5 | R$ 2.300,00 | 45 |
| Método Guloso | 7,2 | R$ 1.950,00 | 0,8 |

## Benefícios da Implementação
1. **Otimização de Recursos**: Alocação eficiente de sensores.
2. **Redução de Riscos**: Proteção das áreas mais vulneráveis.
3. **Automação e Eficiência**: Processo automatizado com resposta rápida a novas ameaças.
4. **Monitoramento Contínuo e Alertas Proativos**: Envio de alertas em casos críticos.

## Conclusão
O uso de algoritmos genéticos proporciona uma solução escalável e eficaz para otimizar a alocação de sensores em infraestruturas de TI, maximizando a proteção ao equilibrar custo e capacidade. Com esta implementação, é possível reduzir vulnerabilidades e garantir uma resposta proativa a incidentes.