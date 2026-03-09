# Splunk Sysmon Detection Lab

Este projeto demonstra a configuração do Splunk Free com Sysmon para detecção de processos suspeitos.

## Tecnologias

- Splunk Free
- Sysmon
- Windows Event Logs

## Detecções criadas

- Execução de PowerShell
- Criação de processos suspeitos
- Monitoramento de CommandLine

## Query exemplo

index=sysmon
| table _time Image User CommandLine ParentImage
| sort -_time
