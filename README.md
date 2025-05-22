# 📚 Microsoft Azure - Resumos, Anotações e Dicas AZ-900

Repositório com material de apoio para estudos e implementações na Azure, focado nos conceitos da certificação AZ-900 e arquitetura de nuvem.

## 📌 Componentes de Arquitetura do Azure

### 🧩 Módulos do Curso AZ-900
O curso está dividido em três módulos principais. Este material cobre:
- **Componentes de arquitetura**: regiões, disponibilidade e organização de recursos
- **Computação e rede**: laboratórios práticos com VMs, armazenamento e redes virtuais
- **Serviços gerenciados**: aplicativos hospedados e soluções de nuvem

### 🌍 Regiões e Disponibilidade
**Conceitos-chave:**
- **Regiões**: Pontos geográficos onde os recursos são hospedados (representados por áreas azuis no mapa Azure)e
- **Regiões anunciadas**: Áreas em preparação (ex: México Central)
- **Fatores de escolha**:
  - Proximidade dos usuários (redução de latência)
  - Conformidade com leis locais (ex: LGPD no Brasil)
  - Custos variáveis por região
  - Disponibilidade de serviços específicos

⚠️ **Importante**: Nem todos os serviços estão disponíveis em todas as regiões. Novos recursos podem ser liberados gradualmente.

### 🏗️ Zonas de Disponibilidade
**Estrutura física:**
1. Cada região possui **mínimo de 3 datacenters** independentes
2. Datacenters possuem:
   - Alimentação elétrica redundante
   - Resfriamento independente
   - Conexão via backbone privado Microsoft

**Vantagens:**
- Tolerância a falhas (se um DC falhar, outros mantêm serviços)
- Replicação síncrona de dados críticos
- SLA elevado (99.99% de disponibilidade)

### 🔄 Pares de Regiões
**Funcionamento:**
- Toda região principal tem uma região-par para disaster recovery
- Atualizações são aplicadas sequencialmente entre pares
- Exemplo: Brasil Sul (principal) → Centro dos EUA (par)

ℹ️ A região do Rio de Janeiro ainda não é um par completo para São Paulo.

## 🏛️ Regiões Soberanas
**Características especiais:**
1. **Azure Government (EUA)**
   - Exclusivo para agências governamentais americanas
   - Infraestrutura fisicamente isolada

2. **Azure China (Operado pela 21Vianet)**
   - Conformidade com leis chinesas
   - Dados permanecem dentro da China
   - Não integrado com nuvem global

## 🗂 Organização de Recursos
### Hierarquia Azure:
1. **Grupos de Gerenciamento** (políticas organizacionais)
2. **Assinaturas** (unidades de cobrança e isolamento)
3. **Grupos de Recursos** (contêineres lógicos)
4. **Recursos** (serviços implantados)

### 💡 Boas Práticas:
- Use grupos de recursos como "caixas organizacionais" por projeto/função
- Uma assinatura pode conter recursos em múltiplas regiões
- É possível mover recursos entre grupos, mas não renomeá-los
- Implemente tags para rastreamento de custos

## 🛠️ Principais Serviços Azure
| Categoria        | Exemplos de Serviços         |
|------------------|------------------------------|
| Computação       | VMs, App Services, AKS       |
| Armazenamento    | Blob Storage, Files, Disks   |
| Rede             | Virtual Network, Load Balancer|
| Segurança        | Azure AD, Security Center    |
| Monitoramento    | Azure Monitor, Log Analytics |

## 📚 Material Complementar
- [Mapa Global de Regiões Azure](https://azure.microsoft.com/en-us/global-infrastructure/geographies/)
- [Laboratórios Microsoft Learn](https://learn.microsoft.com/en-us/training/)
- [Calculadora de Custos Azure](https://azure.microsoft.com/en-us/pricing/calculator/)

---

**Nota**: Este material está em constante atualização. Contribuições são bem-vindas via pull requests!
