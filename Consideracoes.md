Considerações:

Resiliência de Dados:

BD na cloud pública com recursos de replicação e backups automáticos;
políticas de retenção de backups adequadas e validação frequente;
armazenardados em múltiplas zonas de disponibilidade na cloud para aumentar a resiliência contra falhas de hardware ou região;
Redundância de Servidores;

Medidas de Segurança:

Para rede Wifi:
Autenticação WPA2 ou WPA3 com autenticação via Radius;
Filtragem de MAC e Mac Binding;
VLAN segmentada para rede Wifi para gestão e navegação;
Firmware atualizado;

Para servidores:
Atualizações regulares de segurança;
Firewall do Windows e Linux ativado (mesmo com FW de borda).
Alteração das portas padrão.
Política de senha;
Autenticação 2FA com PAM;
Auditorias de Segurança frequentes;
Syslog;
Remoção e disable de serviços desnecessários.
Se não afetar o desempenho, uso de EDR e DLP.
Auditorias de Segurança frequentes. (inclui leitura do syslog habilitado).

Entre as conexões:
Regras de firewall para permitir acesso do backoffice somente as redes e ips necessários. Se possível usar firewall de nextgen que pode validar inclusive o usuário;
Tráfego SSL e Inspeção SSL nas bordas (com exceção das origens válidadas).
acesso aos FWs somente mediante a SSO via SAML com AzureAD ou Radius;

de forma geral:
Utilizar SSO ou Radius e MFA (pelo menos 2FA) através de sistemas de gestão de indentidade e controle de acesso (Okta, OneLogin) somente para gestão de identidiade pode ser usado o próprio AzureAD para SSO.
Monitorar Autenticações; se possível utilizar análise de comportamento.

Observabilidade do sistema:

Utilizar Syslog, ferramentas de monitoramento como Zabbix, Grafana e Prometheus, bem como ferramentas de observabilidade como Datadog e a salada de frutas da Riverbed (diferentes soluções da riverbed monitoram objetos distintos do ambiente como: Aternity EUEM/DEM (enduser/devices
 
experience), Alluvio APM (App Monitor) e Alluvio NPM (observabilidade de rede a nível de Flow e Packets);

Gestão de custos eficiente:
Dimensionamento adequado dos recursos de cloud alocados (fonte de maior custo);
Revisão regular de gastos;
Políticas e triggers de desligamento das instâncias de vm em horários não utilizados e políticas de ociosidade de máquinas para dispositivos windows no Active Directory;
Automação de processos (provisionamento, escalonamento e desativação de recursos);
Análise de CXB;
