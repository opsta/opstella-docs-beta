---
outline: deep
---

## Opstella Reference Architecture

### <ins><strong>Standalone Architecture</strong></ins>

![Opstella Architecture!](/images/intro/reference-architecture/standalone-architecture.svg){data-zoomable}

#### Use Cases 

1. Prove of concept for a whole Opstella and DevSecOps Platform.
2. Testing or staging platform environment.

#### Specification

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-883g{background-color:#ffffff;border-color:#0e0e0e;text-align:center;vertical-align:top}
.tg .tg-4pf1{background-color:#ffffff;border-color:#0e0e0e;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-lioa{background-color:#ffffff;border-color:#0e0e0e;text-align:left;vertical-align:top}
.tg .tg-3ejf{background-color:#D9D9D9;border-color:#0e0e0e;text-align:center;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-lioa"></th>
    <th class="tg-4pf1"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">Number of Nodes</span></th>
    <th class="tg-4pf1"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">CPU Cores</span></th>
    <th class="tg-4pf1"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">Memory (GB)</span></th>
    <th class="tg-4pf1"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">Disk (GB)</span></th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-3ejf" colspan="5"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Virtual Machines</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Bastion Host</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">20</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">HAProxy</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">20</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">NFS Share</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">100</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">GitLab</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">40</span></td>
  </tr>
  <tr>
    <td class="tg-3ejf" colspan="5"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Standalone Cluster</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Kubernetes Master Nodes</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">40</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Kubernetes Worker Nodes</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">5</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">10</span></td>
    <td class="tg-883g"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">40</span></td>
  </tr>
  <tr>
    <td class="tg-4pf1"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">Total</span></td>
    <td class="tg-4pf1"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">10</span></td>
    <td class="tg-4pf1"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">11</span></td>
    <td class="tg-4pf1"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">24</span></td>
    <td class="tg-4pf1"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">260</span></td>
  </tr>
</tbody></table>

#### Network Subnet

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-ycr8{background-color:#ffffff;text-align:left;vertical-align:top}
.tg .tg-px6y{background-color:#D9D9D9;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-i81m{background-color:#ffffff;text-align:center;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-px6y"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Type</span></th>
    <th class="tg-px6y"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Subnet IP</span></th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">1 Kubernetes Clusters Subnet</span></td>
    <td class="tg-i81m"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">192.168.72.0/24</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Pod Subnet (per Cluster)</span></td>
    <td class="tg-i81m"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">172.16.72.0/22</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Service Subnet (per Cluster)</span></td>
    <td class="tg-i81m"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">172.16.76.0/22</span></td>
  </tr>
</tbody></table>


#### Domain

You must provide domains. For example, we will use <strong>*.devops.example.com</strong> and SSL certificates in this reference architecture. These are domains that will be assigned for DevSecOps tools and Opstella.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-ycr8{background-color:#ffffff;text-align:left;vertical-align:top}
.tg .tg-6v43{background-color:#ffffff;font-weight:bold;text-align:left;vertical-align:top}
.tg .tg-px6y{background-color:#D9D9D9;font-weight:bold;text-align:center;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-px6y"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Service Name</span></th>
    <th class="tg-px6y"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Ingress Domain</span></th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-6v43" colspan="2"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">Opstella</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Opstella UI</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">opstella</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Opstella Core</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">opstella-backend</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Opstella Clear Session</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">opstella-clear-session</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Keycloak</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">opstella-idp</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-6v43" colspan="2"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">DevOps Tools</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">ArgoCD</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">argocd</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">DefectDojo</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">defectdojo</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">GitLab</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">gitlab</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Headlamp</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">headlamp</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Harbor</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">harbor</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-6v43" colspan="2"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">DevSecOps Tools</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">SonarQube</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">sonarqube.</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Vault</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">vault</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-6v43" colspan="2"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">Observability Tools</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Loki </span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">loki</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Grafana Dashboard</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">grafana</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Tempo </span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">tempo</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Mimir </span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">mimir</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-6v43" colspan="2"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">Common Services</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">MinIO</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">minio</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">MinIO API</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">minio-api</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
</tbody></table>

#### Ingress

![Opstella Architecture!](/images/intro/reference-architecture/ingress-kubernetes-traffic-flow-standalone.svg){data-zoomable}

#### Firewall

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-rm6k{background-color:#ffffff;color:#1C1E21;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-rtlp{background-color:#ffffff;color:#1C1E21;text-align:center;vertical-align:top}
.tg .tg-vzil{background-color:#D9D9D9;color:#1C1E21;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-7v1e{background-color:#D9D9D9;color:#1C1E21;text-align:center;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Policy</span></th>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Protocol</span></th>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Direction</span></th>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Port</span></th>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Source</span></th>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Description</span></th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-vzil" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">Kubernetes Master Nodes</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">6443</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Any</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Kubernetes API</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">6443</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">HAProxy</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Kubernetes API</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">6443</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Worker Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Kubernetes API</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">9345</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Master Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Supervisor API</span></td>
  </tr>
  <tr>
    <td class="tg-rm6k" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">9345</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Worker Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Supervisor API</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">2379</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Master Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">etcd Client Port</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">2380</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Master Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">etcd Peer Port</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">2381</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Master Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">etcd Metrics Port</span></td>
  </tr>
  <tr>
    <td class="tg-7v1e" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">Kubernetes Worker Nodes</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">30080;30443</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">HAProxy</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">NodePort Ingress Service</span></td>
  </tr>
  <tr>
    <td class="tg-vzil" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">Kubernetes Master &amp; Worker Nodes</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">10250</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Any</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">kubelet Metrics</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">179</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">All RKE2 Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Calico CNI with BGP</span></td>
  </tr>
  <tr>
    <td class="tg-rm6k" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">4789</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">All RKE2 Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Calico CNI with VXLAN</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">5473</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">All RKE2 Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Calico CNI with Typha</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">9098</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">All RKE2 Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Calico Typha health checks</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">9099</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">All RKE2 Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Calico health checks</span></td>
  </tr>
  <tr>
    <td class="tg-7v1e" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">GitLab</span></td>
  </tr>
  <tr>
    <td class="tg-rm6k" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">80;443</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Any</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Web Service</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">22</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Any</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Git SSH</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">9090</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Any</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">GitLab Prometheus Metrics</span></td>
  </tr>
  <tr>
    <td class="tg-7v1e" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">NFS</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP/UDP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">2049</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Worker Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">NFSd</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP/UDP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">111</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Worker Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">PortMapper</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP/UDP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">33333</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Worker Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">MountD</span></td>
  </tr>
  <tr>
    <td class="tg-7v1e" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">HAProxy</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">80;443</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Any</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">HTTP/HTTPS Inbound</span></td>
  </tr>
</tbody></table>

<br/>
<hr/>

### <ins><strong>Multi-Cluster Architecture</strong></ins>

![Opstella Architecture!](/images/intro/reference-architecture/distributed-architecture.svg){data-zoomable}

#### Use Cases 

Scalable deployments for production environments.

#### Specification

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-883g{background-color:#ffffff;border-color:#0e0e0e;text-align:center;vertical-align:top}
.tg .tg-4pf1{background-color:#ffffff;border-color:#0e0e0e;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-lioa{background-color:#ffffff;border-color:#0e0e0e;text-align:left;vertical-align:top}
.tg .tg-3ejf{background-color:#D9D9D9;border-color:#0e0e0e;text-align:center;vertical-align:top}
.tg .tg-4trs{border-color:#0e0e0e;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-6hj9{background-color:#ffffff;border-color:#0e0e0e;font-weight:bold;text-align:left;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-6hj9"></th>
    <th class="tg-4pf1"><span style="font-style:normal;text-decoration:none;color:#000">Number of Nodes</span></th>
    <th class="tg-4pf1"><span style="font-style:normal;text-decoration:none;color:#000">CPU Cores</span></th>
    <th class="tg-4pf1"><span style="font-style:normal;text-decoration:none;color:#000">Memory (GB)</span></th>
    <th class="tg-4pf1"><span style="font-style:normal;text-decoration:none;color:#000">Disk (GB)</span></th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-3ejf" colspan="5"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Virtual Machines</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">Bastion Host</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">20</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">HAProxy</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">20</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">NFS Share (DevSecOps)</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">500</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">NFS Share (Observability)</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">500</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">NFS Share (DEV)</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">100</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">NFS Share (PRD)</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">100</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">GitLab</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">1</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">8</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">40</span></td>
  </tr>
  <tr>
    <td class="tg-3ejf" colspan="5"><span style="font-style:normal;text-decoration:none;color:#000;background-color:transparent">DevSecOps Cluster</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">Kubernetes Master Nodes</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">3</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">20</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">Kubernetes Worker Nodes</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">3</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">8</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">40</span></td>
  </tr>
  <tr>
    <td class="tg-3ejf" colspan="5"><span style="font-style:normal;text-decoration:none;color:#000;background-color:transparent">Observability Cluster</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">Kubernetes Master Nodes</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">3</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">20</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">Kubernetes Worker Nodes</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">3</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">8</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">40</span></td>
  </tr>
  <tr>
    <td class="tg-3ejf" colspan="5"><span style="font-style:normal;text-decoration:none;color:#000;background-color:transparent">DEV Application Workload Cluster</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">Kubernetes Master Nodes</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">3</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">20</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">Kubernetes Worker Nodes</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">3</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">8</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">40</span></td>
  </tr>
  <tr>
    <td class="tg-3ejf" colspan="5"><span style="font-style:normal;text-decoration:none;color:#000;background-color:transparent">PRD Application Workload Cluster</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">Kubernetes Master Nodes</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">3</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">2</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">4</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">20</span></td>
  </tr>
  <tr>
    <td class="tg-lioa"><span style="font-style:normal;text-decoration:none;color:#000">Kubernetes Worker Nodes</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">5</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">6</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">8</span></td>
    <td class="tg-883g"><span style="font-style:normal;text-decoration:none;color:#000">40</span></td>
  </tr>
  <tr>
    <td class="tg-4trs"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Total</span></td>
    <td class="tg-4trs"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">36</span></td>
    <td class="tg-4trs"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">36</span></td>
    <td class="tg-4trs"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">68</span></td>
    <td class="tg-4trs"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">1520</span></td>
  </tr>
</tbody></table>

#### Network Subnet

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-ycr8{background-color:#ffffff;text-align:left;vertical-align:top}
.tg .tg-px6y{background-color:#D9D9D9;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-xmun{background-color:#ffffff;color:#0E0E0E;text-align:left;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-px6y"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Type</span></th>
    <th class="tg-px6y"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Subnet IP</span></th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-ycr8" rowspan="4"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">4 Kubernetes Clusters Subnet</span></td>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">192.168.72.0/24</span></td>
  </tr>
  <tr>
    <td class="tg-xmun"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#0E0E0E">192.168.73.0/24</span></td>
  </tr>
  <tr>
    <td class="tg-xmun"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#0E0E0E">192.168.74.0/24</span></td>
  </tr>
  <tr>
    <td class="tg-xmun"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#0E0E0E">192.168.75.0/24</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Pod Subnet (per Cluster)</span></td>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">172.16.72.0/22</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Service Subnet (per Cluster)</span></td>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">172.16.76.0/22</span></td>
  </tr>
</tbody></table>

#### Domain

You must provide domains. For example, we will use <strong>*.devops.example.com</strong> and SSL certificates in this reference architecture. These are domains that will be assigned for DevSecOps tools and Opstella.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-ycr8{background-color:#ffffff;text-align:left;vertical-align:top}
.tg .tg-m0qo{background-color:#ffffff;color:#0E0E0E;font-weight:bold;text-align:left;vertical-align:top}
.tg .tg-6v43{background-color:#ffffff;font-weight:bold;text-align:left;vertical-align:top}
.tg .tg-px6y{background-color:#D9D9D9;font-weight:bold;text-align:center;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-px6y"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Service Name</span></th>
    <th class="tg-px6y"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Ingress Domain</span></th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-6v43" colspan="2"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">Opstella</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Opstella UI</span></td>
    <td class="tg-m0qo"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">opstella</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Opstella Core</span></td>
    <td class="tg-m0qo"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">opstella-backend</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Opstella Clear Session</span></td>
    <td class="tg-m0qo"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">opstella-clear-session</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Keycloak</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">opstella-idp</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-6v43" colspan="2"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">DevOps Tools</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">ArgoCD (DEV)</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">argocd</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">-dev.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">ArgoCD (PRD)</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">argocd-prd</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">DefectDojo</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">defectdojo</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">GitLab</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">gitlab</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Headlamp</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">headlamp</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Harbor</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">harbor</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-6v43" colspan="2"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">DevSecOps Tools</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">SonarQube</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">sonarqube.</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Vault</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">vault</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-6v43" colspan="2"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">Observability Tools</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Loki </span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">loki</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Grafana Dashboard</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">grafana</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Tempo </span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">tempo</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">Mimir </span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">mimir</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-6v43" colspan="2"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">Common Services</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">MinIO  (DevSecOps)</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">minio-dso</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">MinIO API (DevSecOps)</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">minio-dso-api</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">MinIO (Observability)</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">minio-obs</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
  <tr>
    <td class="tg-ycr8"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">MinIO API (Observability)</span></td>
    <td class="tg-6v43"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000">minio-obs-api</span><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000">.devops.example.com</span></td>
  </tr>
</tbody></table>

#### Ingress

![Opstella Architecture!](/images/intro/reference-architecture/ingress-kubernetes-traffic-flow-distributed.svg){data-zoomable}

#### Firewall

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-rm6k{background-color:#ffffff;color:#1C1E21;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-rtlp{background-color:#ffffff;color:#1C1E21;text-align:center;vertical-align:top}
.tg .tg-vzil{background-color:#D9D9D9;color:#1C1E21;font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-7v1e{background-color:#D9D9D9;color:#1C1E21;text-align:center;vertical-align:top}
</style>
<table class="tg"><thead>
  <tr>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Policy</span></th>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Protocol</span></th>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Direction</span></th>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Port</span></th>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Source</span></th>
    <th class="tg-rm6k"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#1C1E21">Description</span></th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-vzil" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">Kubernetes Master Nodes</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">6443</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">HAProxy</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Kubernetes API</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">6443</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Worker Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Kubernetes API</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">9345</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Master Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Supervisor API</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">9345</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Worker Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Supervisor API</span></td>
  </tr>
  <tr>
    <td class="tg-rm6k" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">2379</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Master Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">etcd Client Port</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">2380</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Master Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">etcd Peer Port</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">2381</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Master Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">etcd Metrics Port</span></td>
  </tr>
  <tr>
    <td class="tg-7v1e" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">Kubernetes Worker Nodes</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">30080;30443</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">HAProxy</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">NodePort Ingress Service</span></td>
  </tr>
  <tr>
    <td class="tg-7v1e" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">Kubernetes Master &amp; Worker Nodes</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">10250</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Any</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">kubelet Metrics</span></td>
  </tr>
  <tr>
    <td class="tg-rm6k" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">179</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">All RKE2 Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Calico CNI with BGP</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">4789</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">All RKE2 Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Calico CNI with VXLAN</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">5473</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">All RKE2 Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Calico CNI with Typha</span></td>
  </tr>
  <tr>
    <td class="tg-rm6k" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">9098</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">All RKE2 Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Calico Typha health checks</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">9099</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">All RKE2 Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Calico health checks</span></td>
  </tr>
  <tr>
    <td class="tg-7v1e" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">GitLab</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">80;443</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Any</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Web Service</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">22</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Any</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Git SSH</span></td>
  </tr>
  <tr>
    <td class="tg-rm6k" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">9090</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Any</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">GitLab Prometheus Metrics</span></td>
  </tr>
  <tr>
    <td class="tg-7v1e" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">NFS</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP/UDP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">2049</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Worker Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">NFSd</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP/UDP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">111</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Worker Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">PortMapper</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rm6k"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP/UDP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">33333</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">RKE2 Worker Nodes</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">MountD</span></td>
  </tr>
  <tr>
    <td class="tg-7v1e" colspan="6"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21;background-color:transparent">HAProxy</span></td>
  </tr>
  <tr>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Allow</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">TCP</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Inbound</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">80;443</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">Any</span></td>
    <td class="tg-rtlp"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#1C1E21">HTTP/HTTPS Inbound</span></td>
  </tr>
</tbody></table>