---
title: Configurar limites de taxa
intro: 'É possível definir limites de taxa no {{ site.data.variables.product.prodname_ghe_server }} usando o {{ site.data.variables.enterprise.management_console }}.'
redirect_from:
  - /enterprise/admin/installation/configuring-rate-limits
versions:
  enterprise-server: '*'
---

### Habilitar limites de taxa para a {{ site.data.variables.product.prodname_enterprise_api }}

Habilitar limites de taxa na {{ site.data.variables.product.prodname_enterprise_api }} pode impedir o uso excessivo de recursos por usuários individuais ou não autenticados. Para obter mais informações, consulte "[Limitação de taxa](/enterprise/{{ currentVersion }}/v3/#rate-limiting)".

{% note %}

**Observação:** o {{ site.data.variables.enterprise.management_console }} lista o período (por minuto ou hora) para cada limite de taxa.

{% endnote %}

{{ site.data.reusables.enterprise_site_admin_settings.access-settings }}
{{ site.data.reusables.enterprise_site_admin_settings.management-console }}
2. Em "Limites de taxa", selecione **Enable API Rate Limiting** (Habilitar limite de taxa da API). ![Caixa de seleção para habilitar limite de taxas de API](/assets/images/enterprise/management-console/api-rate-limits-checkbox.png)
3. Informe os limites para solicitações autenticadas e não autenticadas de cada API ou aceite os limites padrão sugeridos.
{{ site.data.reusables.enterprise_management_console.save-settings }}

### Habilitar limites de taxa de abuso

Definir limites de taxa de abuso protege o nível geral de serviço na {{ site.data.variables.product.product_location_enterprise }}.

{{ site.data.reusables.enterprise_site_admin_settings.access-settings }}
{{ site.data.reusables.enterprise_site_admin_settings.management-console }}
2. Em "Limites de taxa", selecione **Enable Abuse Rate Limiting** (Habilitar limite de taxa de abuso). ![Caixa de seleção para habilitar limite de taxas de abuso](/assets/images/enterprise/management-console/abuse-rate-limits-checkbox.png)
3. Informe os limites para Solicitações totais, Limite de CPU e Limite de CPU para pesquisa ou aceite os limites padrão sugeridos.
{{ site.data.reusables.enterprise_management_console.save-settings }}

### Habilitar limites de taxa do Git

É possível aplicar limites de taxa do Git por rede de repositório ou ID do usuário. Os limites da taxa do Git são expressos em operações simultâneas por minuto e são adaptáveis com base na carga atual da CPU.

{{ site.data.reusables.enterprise_site_admin_settings.access-settings }}
{{ site.data.reusables.enterprise_site_admin_settings.management-console }}
2. Em "Rate Limiting" (Limites de taxa), selecione **Enable Git Rate Limiting** (Habilitar limite de taxa do Git). ![Caixa de seleção para habilitar limite de taxas do Git](/assets/images/enterprise/management-console/git-rate-limits-checkbox.png)
3. Digite limites para cada rede de repositório ou ID do usuário. ![Campos para limites de rede de repositório e ID do usuário](/assets/images/enterprise/management-console/example-git-rate-limits.png)
{{ site.data.reusables.enterprise_management_console.save-settings }}