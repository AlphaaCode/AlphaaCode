<div align="center">

<img src="assets/header.svg" width="100%" alt="Yazid Bensefia, software engineer in bioinformatics and applied AI" />

<br/>

[![Portfolio](https://img.shields.io/badge/%F0%9F%8C%90%20Portfolio-161B22?style=for-the-badge&labelColor=00E5C3)](https://www.bensefiayazid.site/projects)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-161B22?style=for-the-badge&logo=linkedin&logoColor=00E5C3)](https://www.linkedin.com/in/bensefia-yazid-7604a9317/)
[![Email](https://img.shields.io/badge/Email-161B22?style=for-the-badge&logo=gmail&logoColor=00E5C3)](mailto:bensefiayazid@gmail.com)
[![Location](https://img.shields.io/badge/Algiers%2C_Algeria-161B22?style=for-the-badge&logo=googlemaps&logoColor=00E5C3)](https://maps.google.com/?q=Algiers)
[![Followers](https://img.shields.io/github/followers/AlphaaCode?style=for-the-badge&logo=github&logoColor=00E5C3&labelColor=161B22&color=161B22)](https://github.com/AlphaaCode?tab=followers)

</div>

---

## 👨‍💻 About Me

<table>
<tr>
<td width="62%" valign="top">

```console
yazid@algiers:~$ whoami
Yazid Bensefia, software engineer

yazid@algiers:~$ cat now.txt
studying   MSc Bioinformatics @ USTHB (2026)
thesis     federated learning, breast DCE-MRI
ships      Next.js / NestJS / FastAPI / Flutter
languages  FR / EN / AR products, RTL included

yazid@algiers:~$ echo $PROBLEM
medical data is small, imbalanced, locked in hospitals
```

I build models that learn from scans they never get to see, and the apps clinicians use to reach them.

</td>
<td width="38%" align="center" valign="middle">

<img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExeXlxZ3M4bGo3eDRzZmV4cDBtdTBkNWY5NTV1b2pnY3htZG02Z3l6eSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/13pHvqbNfjaZyg/giphy.gif" width="300" alt="Anime hand reaching out" />

</td>
</tr>
</table>

---

## 🧬 The problem I work on

Hospitals can't pool their MRI scans, so no single site has enough data, and what each does have is heavily imbalanced. In my thesis, each hospital trains on its own data against one shared backbone, and only the small classifier heads travel.

```mermaid
flowchart LR
    BB(["🧠 Shared backbone<br/>feature extractor"]):::model

    subgraph HA["🏥 Hospital A"]
        SA[("DCE-MRI<br/>stays on site")]:::data --> HdA["Local head<br/>rebalanced"]:::model
    end
    subgraph HB["🏥 Hospital B"]
        SB[("DCE-MRI<br/>stays on site")]:::data --> HdB["Local head<br/>rebalanced"]:::model
    end
    subgraph HC["🏥 Hospital C"]
        SC[("DCE-MRI<br/>stays on site")]:::data --> HdC["Local head<br/>rebalanced"]:::model
    end

    BB -.->|features| SA
    BB -.->|features| SB
    BB -.->|features| SC
    HdA ==>|"weights only"| AGG
    HdB ==>|"weights only"| AGG
    HdC ==>|"weights only"| AGG
    AGG(["FedSCRT<br/>federated classifier"]):::out

    classDef data fill:#0B3B3F,stroke:#00E5C3,color:#ffffff
    classDef model fill:#161B22,stroke:#6EA8FF,color:#ffffff
    classDef out fill:#00E5C3,stroke:#00E5C3,color:#0D1117
    style HA fill:#0D1117,stroke:#30363D,color:#c9d1d9
    style HB fill:#0D1117,stroke:#30363D,color:#c9d1d9
    style HC fill:#0D1117,stroke:#30363D,color:#c9d1d9
```

<sub>Code: <a href="https://github.com/AlphaaCode/FedSCRT-model">FedSCRT-model</a> · the product around it: <a href="https://github.com/AlphaaCode/fedmri-app">fedmri-app</a></sub>

---

## 🛰️ Tech Stack

<div align="center">

**Daily drivers**

<img src="https://skillicons.dev/icons?i=py,pytorch,ts,nextjs,nestjs,fastapi,postgres,docker&perline=8" />

**Also used**

<img src="https://skillicons.dev/icons?i=js,nodejs,react,tailwind,prisma,supabase,django,flutter,dart,cs,cpp,latex,git,github,linux&perline=15" />

<sub>scikit-learn &nbsp;·&nbsp; Hugging Face &nbsp;·&nbsp; timm &nbsp;·&nbsp; SimpleITK &nbsp;·&nbsp; Flower &nbsp;·&nbsp; TanStack Query &nbsp;·&nbsp; shadcn/ui</sub>

</div>

---

## 🚀 Featured Projects

<table>
<tr>
<td width="50%" valign="top">

### [FedSCRT-model](https://github.com/AlphaaCode/FedSCRT-model)
My thesis code. Federated learning on breast DCE-MRI: 2.5D Gated-Attention MIL, a three-stage imbalance-aware training pipeline, and FedSCRT, which federates locally rebalanced classifier heads over one shared backbone.

`PyTorch` `timm` `LoRA` `SimpleITK` `FastAPI`

</td>
<td width="50%" valign="top">

### [fedmri-app](https://github.com/AlphaaCode/fedmri-app)
The product around the model. A clinician portal (upload, prediction, attention maps, async FL round) and a patient portal over a simulated 3-hospital network, with per-hospital silos enforced at the API.

`Next.js` `NestJS` `Prisma` `PostgreSQL` `FastAPI` `Flower`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [Meayer Frontend](https://github.com/Corsairs-Bejaia/Meayer-Frontend)
Team project. Reviewer console where medical reviewers verify, audit and approve AI-generated medical reports for Algerian digital healthcare. I built the web frontend.

`React` `TanStack Router` `TanStack Query` `Vite` `Tailwind`

</td>
<td width="50%" valign="top">

### [microhack-port-flow](https://github.com/AlphaaCode/microhack-port-flow)
Port logistics app: truck and driver assets, time-slot booking, dispatch dashboard and in-app chat. Supabase auth with middleware-guarded routes.

`Next.js` `TypeScript` `Supabase` `Tailwind`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [SEMART-Fr](https://github.com/AlphaaCode/SEMART-Fr)
Corporate site for an industrial equipment and services company. Fully localized in FR / EN / AR with RTL, an equipment catalogue, case studies and a blog.

`Next.js App Router` `next-intl` `shadcn/ui`

</td>
<td width="50%" valign="top">

### [transasim-mobile](https://github.com/AlphaaCode/transasim-mobile)
White-label eSIM app: one Flutter codebase shipped under several client brands, each with its own theme and launch animation.

`Flutter` `Dart`

</td>
</tr>
</table>

<sub>A lot of my work (client projects, the rest of the research code) lives in private repositories.</sub>

---

## 📊 GitHub Analytics

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=AlphaaCode&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E5C3&icon_color=00E5C3&text_color=FFFFFF&rank_icon=github" height="180" />
&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs?username=AlphaaCode&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E5C3&text_color=FFFFFF&langs_count=8" height="180" />

<br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=AlphaaCode&theme=tokyonight&hide_border=true&background=0D1117&stroke=00E5C3&ring=00E5C3&fire=00E5C3&currStreakLabel=00E5C3&sideLabels=00E5C3&dates=FFFFFF" />

</div>

---

## 🌐 Let's Connect

<div align="center">

<sub>Open to research collaborations and engineering roles in medical AI.</sub>

<br/><br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-161B22?style=for-the-badge&logo=linkedin&logoColor=00E5C3)](https://www.linkedin.com/in/bensefia-yazid-7604a9317/)
[![Portfolio](https://img.shields.io/badge/%F0%9F%8C%90%20Portfolio-161B22?style=for-the-badge&labelColor=00E5C3)](https://www.bensefiayazid.site/projects)
[![Gmail](https://img.shields.io/badge/Gmail-161B22?style=for-the-badge&logo=gmail&logoColor=00E5C3)](mailto:bensefiayazid@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-161B22?style=for-the-badge&logo=github&logoColor=00E5C3)](https://github.com/AlphaaCode)

<br/>

![Profile Views](https://komarev.com/ghpvc/?username=AlphaaCode&color=00E5C3&style=for-the-badge&label=VISITORS)

<img src="assets/footer.svg" width="100%" alt="Thanks for stopping by" />

</div>
