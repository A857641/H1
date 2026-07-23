1- Script_Capacity_VMDS: Agendado via cronjob nos Servers de VMDS para coletar informações da Base, esse script foi gerado de forma emergencial para atender uma solicitação do cliente, pois não existe na empresa uma ferramenta que consiga monitorar a base com o nível de informações que eles precisavam. O script coleta os dados da base VMDS e salva num CSV.
Ganho: Não existe na empresa uma ferramenta que consiga monitorar a base com o nível de informações que eles precisavam, era necessário acessar as máquinas VMDS todos os dias para obter essas infos. 

2- Autmation Agent Pools - Clean Up - Server Linux: Automação via pipeline no Azure Devops para compressão dos arquivos referente aos artefatos baixados da pipeline em Servers Linux de Build que alarmavam várias vezes na semana e gerava muitos chamados.
Script desenvolvido em bash.
Ganho: Perdíamos um tempo grande tendo que analisar o ofensor do alto consumo de disco e ainda executar de forma manual a limpeza. Esse problema ocorria pelo menos 3 vezes na semana.

3- Autmation Agent Pools - Clean Up - Server Windows: Automação via pipeline no Azure Devops para compressão dos arquivos artefatos baixados da pipeline em Servers Windows de Build que alarmavam várias vezes na semana e gerava muitos chamados.
Script desenvolvido em power shell.
Ganho: Perdíamos um tempo grande tendo que analisar o ofensor do alto consumo de disco e ainda executar de forma manual a limpeza. Esse problema ocorria pelo menos 3 vezes na semana.

4- Cronjob-restart-job-controller:  Automação agendada via cronjob no AKS para restart de um Job-Controller do ambiente de QA que para de funcionar aleatoriamente não gerando nenhuma evidência de erro, o problema era resolvido via restart manual.
Ganho: Parou de ser criado chamados relacionados ao problema tratado, pelo menos 3 dias na semana o problema ocorria. O ambiente ficava parado várias horas no dia até que houvesse um restart manual.

5- Cronjob-cleanup-eeror-pods-dev: Automação agendada via cronjob no AKS para deletar Jobs do ambiente de dev com status de erro e crashloopback depois de mais de 24hs, a ideia é limpar a visão da fila e impedir que outro job seja escalado ficando impedido pelo job preso.
Ganho: Melhor visualização da fila de Pods e otimização do ambiente.

6- Cronjob-cleanup-eeror-pods-eo-web: Automação agendada via cronjob no AKS para deletar Jobs do ambiente de eo-web com status de erro e crashloopback depois de mais de 24hs, a ideia é limpar a visão da fila e impedir que outro job seja escalado ficando impedido pelo job preso.
Ganho: Melhor visualização da fila de Pods e otimização do ambiente.

7- Cronjob-cleanup-eeror-pods-qa-atualizado: Automação agendada via cronjob no AKS para deletar Jobs do ambiente de qa com status de erro e crashloopback depois de mais de 24hs, a ideia é limpar a visão da fila e impedir que outro job seja escalado ficando impedido pelo job preso.
Ganho: Melhor visualização da fila de Pods e otimização do ambiente.

8- Script Básico - Linux: Criei vários scripts básicos de linhas de comando que agilizou as demandas críticas que tivemos, como Split e Migração da base VMDS.
Ganho: Agilidade nas demandas que teriam que ser feitas manualmente, também evitando erro humano.


