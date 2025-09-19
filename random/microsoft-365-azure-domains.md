# Microsoft 365 and Azure Domains - Network Requirements

## Microsoft 365 Unified Domains
Microsoft describes these domains as essential to other services:

| ID  | Category | Domain Name               | Purpose                                                                                    | Ports                    |
| --- | -------- | ------------------------- | ------------------------------------------------------------------------------------------ | ------------------------ |
| 184 | Required | `*.cloud.microsoft`       | Dedicated to authenticated user facing Microsoft SaaS product experiences                  | TCP: 443, 80<br>UDP: 443 |
| 184 | Required | `*.static.microsoft`      | Dedicated to static (not customer generated) content hosted on CDNs                        | TCP: 443, 80<br>UDP: 443 |
| 184 | Required | `*.usercontent.microsoft` | Content used in Microsoft 365 experiences that requires domain isolation from applications | TCP: 443, 80<br>UDP: 443 |

## Office Online FQDNs

| ID | Category | Express Route | Addresses | Ports |
|----|----------|---------------|-----------|-------|
| 46 | Allow<br>Required | Yes | `*.officeapps.live.com`, `*.online.office.com`, `office.live.com`<br>13.107.6.171/32, 13.107.18.15/32, 13.107.140.6/32, 52.108.0.0/14, 52.244.37.168/32, 2603:1006:1400::/40, 2603:1016:2400::/40, 2603:1026:2400::/40, 2603:1036:2400::/40, 2603:1046:1400::/40, 2603:1056:1400::/40, 2603:1063:2000::/38, 2620:1ec:c::15/128, 2620:1ec:8fc::6/128, 2620:1ec:a92::171/128, 2a01:111:f100:2000::a83e:3019/128, 2a01:111:f100:2002::8975:2d79/128, 2a01:111:f100:2002::8975:2da8/128, 2a01:111:f100:7000::6fdd:6cd5/128, 2a01:111:f100:a004::bfeb:88cf/128 | TCP: 443, 80 |
| 47 | Default<br>Required | No | `*.office.net` | TCP: 443, 80<br>UDP: 443 |
| 49 | Default<br>Required | No | `*.onenote.com` | TCP: 443 |
| 50 | Default<br>Optional<br>*Notes: OneNote notebooks (wildcards)* | No | `*.microsoft.com` | TCP: 443 |
| 51 | Default<br>Required | No | `*cdn.onenote.net` | TCP: 443 |
| 53 | Default<br>Required | No | `ajax.aspnetcdn.com`, `apis.live.net`, `officeapps.live.com`, `www.onedrive.com` | TCP: 443 |
| 56 | Allow<br>Required | Yes | `*.auth.microsoft.com`, `*.msftidentity.com`, `*.msidentity.com`, `account.activedirectory.windowsazure.com`, `accounts.accesscontrol.windows.net`, `adminwebservice.microsoftonline.com`, `api.passwordreset.microsoftonline.com`, `autologon.microsoftazuread-sso.com`, `becws.microsoftonline.com`, `ccs.login.microsoftonline.com`, `clientconfig.microsoftonline-p.net`, `companymanager.microsoftonline.com`, `device.login.microsoftonline.com`, `graph.microsoft.com`, `graph.windows.net`, `login-us.microsoftonline.com`, `login.microsoft.com`, `login.microsoftonline-p.com`, `login.microsoftonline.com`, `login.windows.net`, `logincert.microsoftonline.com`, `loginex.microsoftonline.com`, `nexus.microsoftonline-p.com`, `passwordreset.microsoftonline.com`, `provisioningapi.microsoftonline.com`<br>20.20.32.0/19, 20.190.128.0/18, 20.231.128.0/19, 40.126.0.0/18, 2603:1006:2000::/48, 2603:1007:200::/48, 2603:1016:1400::/48, 2603:1017::/48, 2603:1026:3000::/48, 2603:1027:1::/48, 2603:1036:3000::/48, 2603:1037:1::/48, 2603:1046:2000::/48, 2603:1047:1::/48, 2603:1056:2000::/48, 2603:1057:2::/48 | TCP: 443, 80 |

## Additional Required Office 365 Domains

| ID | Category | Required | Domain Name | Ports |
|----|----------|----------|------------|-------|
| 59 | Default<br>Required | No | `*.hip.live.com`, `*.microsoftonline-p.com`, `*.microsoftonline.com`, `*.msauth.net`, `*.msauthimages.net`, `*.msecnd.net`, `*.msftauth.net`, `*.msftauthimages.net`, `*.phonefactor.net`, `enterpriseregistration.windows.net` | TCP: 443, 80 |
| 64 | Allow<br>Required | Yes | `*.protection.office.com`, `*.security.microsoft.com`, `compliance.microsoft.com`, `defender.microsoft.com`, `protection.office.com`, `purview.microsoft.com`, `security.microsoft.com`<br>13.107.6.192/32, 13.107.9.192/32, 2620:1ec:4::192/128, 2620:1ec:a92::192/128 | TCP: 443 |
| 66 | Default<br>Required | No | `*.portal.cloudappsecurity.com` | TCP: 443 |
| 69 | Default<br>Required | No | `*.aria.microsoft.com`, `*.events.data.microsoft.com` | TCP: 443 |
| 70 | Default<br>Required | No | `*.o365weve.com`, `amp.azure.net`, `appsforoffice.microsoft.com`, `assets.onestore.ms`, `auth.gfx.ms`, `c1.microsoft.com`, `dgps.support.microsoft.com`, `docs.microsoft.com`, `msdn.microsoft.com`, `platform.linkedin.com`, `prod.msocdn.com`, `shellprod.msocdn.com`, `support.microsoft.com`, `technet.microsoft.com` | TCP: 443 |
| 71 | Default<br>Required | No | `*.office365.com` | TCP: 443, 80 |
| 73 | Default<br>Required | No | `*.aadrm.com`, `*.azurerms.com`, `*.informationprotection.azure.com`, `ecn.dev.virtualearth.net`, `informationprotection.hosting.portal.azure.net` | TCP: 443 |
| 78 | Default<br>Optional<br>*Notes: Some Office 365 features require endpoints within these domains (including CDNs)* | No | `*.microsoft.com`, `*.msocdn.com`, `*.onmicrosoft.com` | TCP: 443, 80 |
| 79 | Default<br>Required | No | `o15.officeredir.microsoft.com`, `officepreviewredir.microsoft.com`, `officeredir.microsoft.com`, `r.office.microsoft.com` | TCP: 443, 80 |
| 83 | Default<br>Required | No | `activation.sls.microsoft.com` | TCP: 443 |
| 84 | Default<br>Required | No | `crl.microsoft.com` | TCP: 443, 80 |
| 86 | Default<br>Required | No | `office15client.microsoft.com`, `officeclient.microsoft.com` | TCP: 443 |
| 89 | Default<br>Required | No | `go.microsoft.com` | TCP: 443, 80 |
| 91 | Default<br>Required | No | `ajax.aspnetcdn.com`, `cdn.odc.officeapps.live.com` | TCP: 443, 80 |
| 92 | Default<br>Required | No | `officecdn.microsoft.com`, `officecdn.microsoft.com.edgesuite.net`, `otelrules.azureedge.net` | TCP: 443, 80 |
| 117 | Default<br>Optional<br>*Notes: Yammer* | No | `*.yammer.com`, `*.yammerusercontent.com` | TCP: 443 |
| 122 | Default<br>Optional<br>*Notes: Sway CDNs* | No | `eus-www.sway-cdn.com`, `eus-www.sway-extensions.com`, `wus-www.sway-cdn.com`, `wus-www.sway-extensions.com` | TCP: 443 |
| 125 | Default<br>Required | No | `*.entrust.net`, `*.geotrust.com`, `*.omniroot.com`, `*.public-trust.com`, `*.symcb.com`, `*.symcd.com`, `*.verisign.com`, `*.verisign.net`, `cacerts.digicert.com`, `cert.int-x3.letsencrypt.org`, `crl.globalsign.com`, `crl.globalsign.net`, `crl.identrust.com`, `crl3.digicert.com`, `crl4.digicert.com`, `isrg.trustid.ocsp.identrust.com`, `mscrl.microsoft.com`, `ocsp.digicert.com`, `ocsp.globalsign.com`, `ocsp.msocsp.com`, `ocsp2.globalsign.com`, `ocspx.digicert.com`, `oneocsp.microsoft.com`, `secure.globalsign.com`, `www.digicert.com`, `www.microsoft.com` | TCP: 443, 80 |
| 147 | Default<br>Required | No | `*.office.com`, `www.microsoft365.com` | TCP: 443, 80 |
| 153 | Default<br>Required | No | `*.azure-apim.net`, `*.flow.microsoft.com`, `*.powerapps.com`, `*.powerautomate.com` | TCP: 443 |
| 156 | Default<br>Required | No | `*.activity.windows.com`, `activity.windows.com` | TCP: 443 |
| 158 | Default<br>Required | No | `*.cortana.ai` | TCP: 443 |
| 159 | Default<br>Required | No | `admin.microsoft.com` | TCP: 443, 80 |
| 160 | Default<br>Required | No | `cdn.odc.officeapps.live.com`, `cdn.uci.officeapps.live.com` | TCP: 443, 80 |
| 184 | Default<br>Required | No | `*.cloud.microsoft`, `*.static.microsoft`, `*.usercontent.microsoft` | - |

## Azure Portal Authentication
Required URLs for Azure portal authentication:

- `login.microsoftonline.com`
- `*.aadcdn.msftauth.net`
- `*.aadcdn.msftauthimages.net`
- `*.aadcdn.msauthimages.net`
- `*.logincdn.msftauth.net`
- `login.live.com`
- `*.msauth.net`
- `*.aadcdn.microsoftonline-p.com`
- `*.microsoftonline-p.com`

## Azure Portal Framework
- `*.portal.azure.com`
- `*.hosting.portal.azure.net`
- `*.reactblade.portal.azure.net`
- `management.azure.com`
- `*.ext.azure.com`
- `*.graph.windows.net`
- `*.graph.microsoft.com`
- `hosting.partners.azure.net`

## User Account Data
- `*.account.microsoft.com`
- `*.bmx.azure.com`
- `*.subscriptionrp.trafficmanager.net`
- `*.signup.azure.com`

## Azure Services
The follo:

| Service Category | Domain Names |
|-----------------|--------------|
| Microsoft Short URL | `aka.ms` |
| Analysis Services | `*.asazure.windows.net` |
| AzConfig Service | `*.azconfig.io` |
| Microsoft Entra | `*.aad.azure.com`, `*.aadconnecthealth.azure.com`, `ad.azure.com`, `api.azrbac.mspim.azure.com`, `appmanagement.activedirectory.microsoft.com`, `elm.iga.azure.com`, `identitygovernance.azure.com`, `iga.azure.com`, `mspim.azure.com`, `*.msidentity.com`, `api.aadrm.com`, `informationprotection.azure.com` |
| Azure Data Factory | `adf.azure.com` |
| Log Analytics | `api.loganalytics.io` |
| Application Insights | `*.applicationinsights.azure.com` |
| App Services | `appservice.azure.com` |
| Azure Arc | `*.arc.azure.net` |
| Azure Bastion | `bastion.azure.com` |
| Azure Batch | `batch.azure.com` |
| Azure Marketplace | `catalogapi.azure.com`, `catalogartifact.azureedge.net`, `gallery.azure.com`, `marketplacedataprovider.azure.com`, `marketplaceemail.azure.com` |
| Change Analysis | `changeanalysis.azure.com` |
| Cognitive Services | `cognitiveservices.azure.com` |
| Microsoft Office | `config.office.com` |
| Azure Cosmos DB | `cosmos.azure.com` |
| SQL Server | `*.database.windows.net` |
| Azure Data Lake | `datalake.azure.net` |
| Azure DevOps | `dev.azure.com` |
| Azure Synapse | `dev.azuresynapse.net` |
| Azure Digital Twins | `digitaltwins.azure.net` |
| Azure Event Hubs | `eventhubs.azure.net` |
| Azure Functions | `functions.azure.com` |
| Azure Kusto | `help.kusto.windows.net`, `kusto.windows.net` |
| Documentation | `go.microsoft.com`, `learn.microsoft.com` |
| Logic Apps | `logic.azure.com` |
| Azure Media Services | `media.azure.net`, `rest.media.azure.net` |
| Azure Monitor | `monitor.azure.com` |
| Azure Network | `network.azure.com` |
| Azure Purview | `purview.azure.com` |
| Azure Quantum | `quantum.azure.com` |
| Azure Search | `search.azure.com` |
| Azure Service Bus | `servicebus.azure.net`, `servicebus.windows.net` |
| Azure Command Shell | `shell.azure.com` |
| Azure Sphere | `sphere.azure.net` |
| Azure Status | `azure.status.microsoft` |
| Azure Storage | `storage.azure.com`, `storage.azure.net` |
| Azure Key Vault | `vault.azure.net` |
| Azure Cloud Shell | `ux.console.azure.com` |

## Third-Party Services
Microsoft recommends these third-party services for use with Microsoft 365 and other Microsoft services:

- `*.akadns.net`
- `*.akam.net`
- `*.akamai.com`
- `*.akamai.net`
- `*.akamaiedge.net`
- `*.akamaihd.net`
- `*.akamaized.net`
- `*.edgekey.net`
- `*.edgesuite.net`

## Windows Virtual Machine Activation
- `azkms.core.windows.net`
- `kms.core.windows.net`