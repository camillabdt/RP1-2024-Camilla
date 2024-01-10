# RP1-2024-Camilla

# Agendamento de Refeições Escolares
Este repositório contém todos os arquivos e documentações relacionados ao projeto "Agendamento de Refeições Escolares". O sistema foi desenvolvido para otimizar e gerenciar o processo de agendamento de refeições em um ambiente escolar. Ele oferece uma interface intuitiva para que alunos, servidores e equipe administrativa possam interagir de maneira eficaz com o sistema.

Link para o Trello
https://trello.com/invite/b/iu1qOrFj/ATTI57d03ecf443857361a5eb327ec307beaF1E03E25/resolucao-de-problemas-i

## Histórias de Usuário (HU)

* HU01: **Como secretaria**, quero cadastrar e atualizar informações dos usuários para organizar o processo de agendamentos de refeição.
* HU02: **Como secretaria**, quero fazer a integração dos dados com base nos dados existentes no sistema da escola para que haja rapidez no processo de cadastro.
* HU03: **Como secretaria**, quero fazer a liberação do sistema, quando houver bloqueio parcial devido a repetição tripla de não presença após agendamento para que o aluno consiga fazer o agendamento.
* HU04: **Como secretaria**, quero assegurar que o sistema contenha os dados dos alunos corretamente e atualizados para que não ocorra inconsistência na hora do agendamento da refeição.
* HU05: **Como aluno/servidor**, quero agendar minhas refeições para que eu possa planejar minha janta.
* HU06: **Como aluno/servidor**, quero visualizar o cardápio semanal para que eu possa confirmar o agendamento ou não.
* HU07: **Como aluno/servidor**, quero ter acesso a possíveis mudanças no cardápio para que possa decidir se vou ou não fazer o agendamento da refeição.
* HU08: **Como aluno/servidor**, quero ser notificado quando não houver refeições no dia para que eu não vá ao refeitório em vão.
* HU09: **Como administração da escola**, quero gerenciar todos os agendamentos para que eu tenha controle do fluxo.
* HU10: **Como administração da escola**, quero ter acesso a lista de todos os usuários do agendamento de refeições para que assegure que está funcionando de maneira satisfatória.
* HU11: **Como administração da escola**, quero poder modificar os cardápios para que quando os auxiliares de cozinha não conseguirem o sistema funcionar.
* HU12: **Como administração da escola**, quero ter controle de quantos alunos em média vão ao refeitório para que consiga fazer gráficos mostrando, por exemplo, dias de maior demanda.
* HU13: **Como equipe da cozinha**, quero enviar informações dos cardápios para o sistema para que os usuários possam verificar os pratos servidos semanalmente.
* HU14: **Como equipe da cozinha**, quero modificar informações dos cardápios, quando necessário, para que o sistema seja atualizado e assegurar a adesão.
* HU15: **Como equipe da cozinha**, quero atualizar o cardápio caso não haja refeição no dia para que os usuários não façam o agendamento no dia.
* HU16: **Como equipe da cozinha**, quero analisar a quantidade de pessoas que agendaram refeições no dia, para que eu prepare somente a quantidade de alimentos necessários.
* HU17: **Como equipe do refeitório**, quero validar os QR codes gerados após agendamento para que possa confirmar ou não o agendamento do usuário.
* HU18: **Como equipe do refeitório**, quero verificar a lista dos usuários agendados para verificar se todos os QR codes aproximados foram contabilizados.
* HU19: **Como equipe do refeitório**, quero ter acesso a todos os agendamentos feitos no dia para caso algum usuário não agendar possa verificar a disponibilidade com a cozinha.
* HU20: **Como cozinha**, quero colocar o estoque no sistema para a administração controlar.
* HU21: **Como administração**, quero poder verificar o estoque para que eu possa comprar ou não mais produtos.
* HU22: **Como cozinha**, quero colocar os produtos usados no dia para que a administração possa ter controle.

## Requisitos Não Funcionais (RNF)

* RNF1: A interface deve ser intuitiva e fácil de usar.
* RNF2: As respostas devem ser rápidas do sistema.
* RNF3: Deve haver uma proteção de dados pessoais e informações de agendamento.
* RNF4: O sistema de ter a capacidade de suportar um grande número de usuários simultâneos.
* RNF5: Deve haver uma alta disponibilidade e baixa taxa de erros.
* RNF6: O sistema deve funciona em diferentes dispositivos e sistemas operacionais.
* RNF7: Deve haver segurança na gestão e verificação de dados pessoais dos usuários.
* RNF8: Deve ocorrer a integração eficiente com a base de dados existente da escola para a automação eficiente do agendamento.
* RNF9: O sistema deve ser adaptável, para permitir acessos por diferentes dispositivos (computadores, tablets, smartphones).
* RNF10: O sistema deve ter a capacidade de gerar relatórios detalhados das listas de agendamento para a cozinha e gestão.
* RNF11: O sistema deve implementar um mecanismo de backup automático para garantir a integridade e a recuperação de dados.

## Regras de Negócio (RN)

* RN01: A refeição só é servida após a validação do QR code gerado pelo sistema de agendamentos.
* RN02: Após três falhas em comparecer ao agendamento, o usuário é bloqueado e requer desbloqueio, feito pela secretaria.
* RN03: Relatórios do sistema de agendamento são gerados toda sexta-feira para análise administrativa.
* RN04: Usuários podem cancelar seus agendamentos de refeições, e a cozinha deve ser notificada desses cancelamentos.
* RN05: O sistema deve enviar notificações automáticas aos usuários sobre falta de refeições no dia, preferencialmente com 24 horas de antecedência.
* RN06: O cardápio semanal deve ser atualizado no sistema de agendamento, pela equipe da cozinha e/ou administração até o domingo da semana anterior.
* RN07: Agendamentos para refeições devem ser feitos até as 19:30 do dia da refeição. Após este horário, o sistema bloqueará agendamentos para este dia, podendo somente agendar para o dia seguinte.
* RN08: Se houver alteração do cardápio com menos de 48 horas antes das refeições, então haverá uma notificação do sistema ao usuário que houve mudanças.
* RN09: Uma lista com todos os agendamentos será gerada automaticamente após as 19:30 e enviada para a cozinha e gestão do sistema para preparação e controle.
* RN10: Para acesso à refeição, o usuário deve apresentar o QR code gerado no momento do agendamento. O sistema de leitura de QR code deve validar a autenticidade e a validade do código.
* RN11: Durante o agendamento, devem ser coletadas informações do usuário, incluindo nome, CPF, status (aluno ou servidor), e opcionalmente uma foto, para fins de identificação e segurança.
* RN12: O sistema de agendamentos deve integrar-se à base de dados existente da secretaria para verificação e cadastro de usuários, garantindo a consistência das informações.
* RN13: uma vez publicado, o cardápio deve estar visível para todos os usuários sem restrições.