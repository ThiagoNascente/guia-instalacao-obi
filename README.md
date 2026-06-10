bash# Acesse a pasta onde o download foi feito (ajuste se não for a Área de Trabalho)
cd ~/Desktop

# Mova o arquivo para o diretório de binários locais do sistema
sudo mv ExamLock-1.0.7-x64-Portable.exe /usr/local/bin/examlock

# Mude o proprietário para o usuário root
sudo chown root:root /usr/local/bin/examlock
sudo chown suporte:suporte /usr/local/bin/examlock

# Dê permissão de leitura e execução para todos, mas escrita apenas para o root (755)
sudo chmod 755 /usr/local/bin/examlock

# Crie o arquivo de atalho diretamente na Área de Trabalho do aluno
sudo nano /home/aluno/"Área de Trabalho"/examlock.desktop

cole o seguinte conteúdo dentro do editor de texto que vai aparecer
ini
[Desktop Entry]
Version=1.0
Type=Application
Name=ExamLock OBI
Exec=/usr/local/bin/examlock
Icon=system-run
Terminal=false
Categories=Education;

ctrl + O para salvart ctrl x para sair

Garanta que o aluno seja o dono do atalho e que o Ubuntu permita a execução dele.bash# Altere o proprietário do atalho para o usuário aluno
sudo chown aluno:aluno /home/aluno/"Área de Trabalho"/examlock.desktop

# Dê permissão de execução ao atalho
sudo chmod +x /home/aluno/"Área de Trabalho"/examlock.desktop

4. Ativar o Ícone (Ação no perfil do Aluno)Por segurança, o Ubuntu desativa novos atalhos de área de trabalho até que o usuário os autorize. 
Quando você logar na conta do Aluno, haverá um ícone com um "X" ou sinal de alerta na Área de Trabalho.

1. Faça login na conta do Aluno.
2. Clique com o botão direito no ícone do ExamLock na Área de Trabalho.
3. Selecione a opção "Permitir Lançamento" (ou "Allow Launching").O ícone mudará de formato e o programa abrirá normalmente com um duplo clique, sem pedir nenhuma senha.
