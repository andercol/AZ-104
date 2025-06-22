### SSPR - Self-Service Password Reset

**SSPR permite que os usuários redefinam suas próprias senhas de forma segura, sem a necessidade de intervenção do help desk de TI.** Pense nisso como uma ferramenta de autonomia para o usuário e de alívio para a equipe de suporte.

#### Como Funciona o SSPR?

1. **Registro de Métodos de Autenticação:** Para usar o SSPR, os usuários precisam registrar previamente um ou mais métodos de verificação (como número de celular, endereço de e-mail alternativo, ou perguntas de segurança) no seu perfil do Microsoft Entra ID.
2. **Processo de Redefinição:**
    - Quando um usuário esquece sua senha, ele navega para a página de login do Microsoft 365, Azure, ou qualquer aplicativo integrado ao Entra ID.
    - Clica na opção "Esqueci minha senha" ou "Não consigo acessar minha conta".
    - O sistema solicita que ele prove sua identidade usando os métodos de autenticação que ele registrou (por exemplo, receber um código por SMS no celular, ou responder às perguntas de segurança).
    - Após a verificação bem-sucedida, o usuário pode definir uma nova senha.
3. **Sincronização:** Se você estiver usando o Azure AD Connect para sincronizar senhas de um ambiente Active Directory local, o SSPR pode ser configurado para redefinir a senha também no ambiente local, garantindo que a nova senha seja consistente em ambos os locais.

#### Benefícios Chave do SSPR:

- **Redução de Custos e Carga do Help Desk:** Diminui drasticamente o volume de chamadas e tickets relacionados a redefinição de senha, liberando a equipe de TI para tarefas mais estratégicas.
- **Melhora da Produtividade do Usuário:** Os usuários podem recuperar o acesso às suas contas instantaneamente, sem esperar pelo suporte, o que minimiza o tempo de inatividade.
- **Segurança Aprimorada:** O SSPR utiliza métodos de verificação seguros para garantir que apenas o usuário legítimo possa redefinir sua senha. Você pode exigir múltiplos fatores de autenticação para o processo de redefinição, tornando-o ainda mais seguro.
- **Experiência do Usuário Aprimorada:** Oferece uma experiência mais suave e autônoma para os usuários.

-------
#### Links de referência:

[Considerações de implantação da redefinição de senha self-service do Microsoft Entra - Microsoft Entra ID | Microsoft Learn](https://learn.microsoft.com/pt-br/entra/identity/authentication/concept-sspr-deploy)
[Habilitar a redefinição de senha self-service do Microsoft Entra - Microsoft Entra ID | Microsoft Learn](https://learn.microsoft.com/pt-br/entra/identity/authentication/tutorial-enable-sspr)
[Políticas de redefinição de senha de autoatendimento - Microsoft Entra ID | Microsoft Learn](https://learn.microsoft.com/pt-br/entra/identity/authentication/concept-sspr-policy)
[Aprofundamento de redefinição de senha self-service - Microsoft Entra ID | Microsoft Learn](https://learn.microsoft.com/pt-br/entra/identity/authentication/concept-sspr-howitworks)
[Habilitar a reversão de senha do Microsoft Entra - Microsoft Entra ID | Microsoft Learn](https://learn.microsoft.com/pt-br/entra/identity/authentication/tutorial-enable-sspr-writeback)
