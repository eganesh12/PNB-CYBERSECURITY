# 🛡️ PNB CyberShield — Cybersecurity Hackathon 2026

> **Live Demo:** [https://c-navy-sigma.vercel.app](https://c-navy-sigma.vercel.app)
>
> 
>**********   sign in interfce      **********
> <img width="1906" height="902" alt="image" src="https://github.com/user-attachments/assets/40ab0c15-7f5d-42b2-af6d-b918ebc45cb3" />                     
                                                     *********        home page *********
<img width="1869" height="913" alt="image" src="https://github.com/user-attachments/assets/82bfafe8-b37f-414e-8f0b-b44d42516160" />

[PNB_CyberShield_Prototype_Guide.pdf](https://github.com/user-attachments/files/26373314/PNB_CyberShield_Prototype_Guide.pdf)

A full-stack cybersecurity dashboard prototype built for the **Punjab National Bank Cybersecurity Hackathon 2026**, featuring Post-Quantum Cryptography (PQC) readiness assessment, asset discovery, certificate generation with QR verification, and AI-powered threat analytics.

---

## 📸 Preview

| Login Page | Dashboard | Certificate |
|---|---|---|
| 3D animated background with globe, matrix rain, stars | KPI cards, asset inventory, crypto overview | Canvas-rendered cert with QR code |

---

## ✨ Features

### 🔐 Authentication
- Email/password login with validation and shake animation
- **Google Sign-In** (OAuth 2.0 via Google Identity Services)
- User avatar + dropdown menu in header
- Sign out with session reset

### 🏠 Dashboard
- KPI cards — Total Assets, Public Web Apps, APIs, Servers, Expiring Certs, High Risk Assets
- Asset Type Distribution donut chart
- Asset Risk Distribution bar chart
- Certificate Expiry Timeline
- IP Version Breakdown
- Asset Inventory table with scan status, cert validity, key length
- Nameserver Records resolver
- Crypto & Security Overview table
- Live activity bar

### 🛸 Asset Inventory
- Full asset table with risk badges, cert status, key length
- Add Asset modal
- Scan All — animated per-asset scanning with TLS/key/risk results
- Apply scan results back to table

### 🏛 Asset Discovery
- **Domain/URL input** — enter any domain or URL to discover assets
- **Time period selector** — 24h / 7d / 30d / 90d / Custom date range
- Animated scan progress (DNS → subdomains → ports → TLS → risk)
- Dynamic network graph — root domain at center, discovered assets orbiting
  - Node border color = risk level (green/amber/red/critical)
  - Animated data packets flowing along edges
- Discovered assets table with IP, type, open ports, TLS version, risk, first-seen date

### 🧬 CBOM (Cryptographic Bill of Materials)
- Key Length Distribution bar chart
- Cipher Usage breakdown with progress bars
- Top Certificate Authorities
- Encryption Protocols donut chart
- Per-application CA table

### 🚶 PQC Posture Dashboard
- Elite-PQC Ready / Standard / Legacy / Critical breakdown
- Assets by Classification Grade
- Application Status donut
- Risk Overview grid
- PQC Support table per asset
- Improvement Recommendations

### ⭐ Cyber Rating
- Consolidated score: **755/1000 — Elite-PQC**
- Tier table (Legacy < 400, Standard 400–700, Elite > 700)

### 📊 Reporting
- Executive Summary
- Scheduled Reports
- On-Demand Reports

### 🏅 Certificate Generation
- Multi-step wizard (Form → Progress → Result)
- Canvas-rendered certificate with:
  - Shield logo, gold borders, corner ornaments, diagonal watermark
  - Domain, org, cert type, key size, issued/expiry dates, cert ID, status
  - **Verified seal** (bottom-left)
  - **QR code** (bottom-right) — auto-generated, links to verify page
- Side QR panel with "Save QR" button
- Download PNG + PEM
- Share / Copy PEM

### 🔍 Certificate Verification (`verify.html`)
- Standalone page — opens instantly when QR is scanned
- Shows: Cert ID, Domain, Org, Type, Key Size, Issued Date, Expiry Date, Status
- Live scan timestamp
- No app loading — pure HTML + URL params

### 🌐 Global Search
- Search assets, domains, IPs, certificates from header
- Fuzzy match with highlighted results
- Click to navigate to relevant page

### 🎨 3D Login Background
- Deep space nebula with drifting color blobs
- 200 twinkling stars
- Matrix rain (crypto characters: `01`, katakana, `∑∆Ω`)
- 3D rotating globe with 4 orbital rings of colored nodes
- Expanding pulse rings from center
- Floating shield particles drifting upward
- Hex grid overlay
- Vignette effect

---

## 🗂 Project Structure

```
├── index.html      # Main app (single-page application)
├── verify.html     # Certificate verification page (opened by QR scan)
└── README.md       # This file
```

---

## 🚀 Getting Started

### Run Locally
Just open `index.html` in any modern browser — no build step, no dependencies.

```bash
# Or serve with any static server
npx serve .
# → http://localhost:3000
```

### Deploy to Vercel
```bash
npm i -g vercel
vercel deploy --yes --prod
```

---

## 🔑 Login Credentials

| Email | Password |
|-------|----------|
| `hackathon_user@pnb.bank.in` | `password` |
| `admin@pnb.bank.in` | `admin123` |
| `admin` | `admin` |

Or use **Continue with Google** (any Gmail account).

---

## 🔧 Google OAuth Setup

1. Go to [console.cloud.google.com](https://console.cloud.google.com)
2. APIs & Services → Credentials → Create OAuth 2.0 Client ID
3. Application type: **Web application**
4. Authorised JavaScript origins: `https://your-domain.vercel.app`
5. Replace `data-client_id` in `index.html` with your Client ID

Current Client ID is configured for `https://c-navy-sigma.vercel.app`.

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Vanilla HTML5, CSS3, JavaScript (ES6+) |
| Charts | Canvas 2D API (custom drawn) |
| Fonts | Google Fonts — Orbitron, Rajdhani, Share Tech Mono |
| QR Code | Google Chart API + qrserver.com fallback |
| Auth | Google Identity Services (GSI) |
| Deployment | Vercel |

---

## 📱 Certificate QR Flow

```
Generate Certificate
       ↓
QR encodes: https://c-navy-sigma.vercel.app/verify.html
            ?verify=PNB-XXXXX
            &domain=portal.pnb.bank.in
            &org=Punjab+National+Bank
            &type=TLS%2FSSL
            &bits=4096
            &issued=29+Mar+2026
            &expires=29+Mar+2027
            &serial=3E:25:F7
       ↓
User scans QR → verify.html opens instantly
       ↓
Shows full certificate details + live scan timestamp
```

---

##
- **Theme:** Post-Quantum Cryptography Readiness
- **Focus Areas:** Asset Discovery, CBOM, PQC Posture, Cyber Rating
- 

---

## 📄 License
[Uploading PNB_CyberShield_Prototype_Guide (1).pdf…]()

MIT — free to use, modify and distribute.
[Uploading PNB_CyberShie%PDF-1.4
%���� ReportLab Generated PDF document (opensource)
1 0 obj
<<
/F1 2 0 R /F2 3 0 R /F3 6 0 R
>>
endobj
2 0 obj
<<
/BaseFont /Helvetica /Encoding /WinAnsiEncoding /Name /F1 /Subtype /Type1 /Type /Font
>>
endobj
3 0 obj
<<
/BaseFont /Helvetica-Bold /Encoding /WinAnsiEncoding /Name /F2 /Subtype /Type1 /Type /Font
>>
endobj
4 0 obj
<<
/Contents 20 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
5 0 obj
<<
/Contents 21 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
6 0 obj
<<
/BaseFont /Helvetica-Oblique /Encoding /WinAnsiEncoding /Name /F3 /Subtype /Type1 /Type /Font
>>
endobj
7 0 obj
<<
/Contents 22 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
8 0 obj
<<
/Contents 23 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
9 0 obj
<<
/Contents 24 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
10 0 obj
<<
/Contents 25 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
11 0 obj
<<
/Contents 26 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
12 0 obj
<<
/Contents 27 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
13 0 obj
<<
/Contents 28 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
14 0 obj
<<
/Contents 29 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
15 0 obj
<<
/Contents 30 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
16 0 obj
<<
/Contents 31 0 R /MediaBox [ 0 0 595.2756 841.8898 ] /Parent 19 0 R /Resources <<
/Font 1 0 R /ProcSet [ /PDF /Text /ImageB /ImageC /ImageI ]
>> /Rotate 0 /Trans <<

>> 
  /Type /Page
>>
endobj
17 0 obj
<<
/PageMode /UseNone /Pages 19 0 R /Type /Catalog
>>
endobj
18 0 obj
<<
/Author (PNB Hackathon 2026) /CreationDate (D:20260331091833+00'00') /Creator (\(unspecified\)) /Keywords () /ModDate (D:20260331091833+00'00') /Producer (ReportLab PDF Library - \(opensource\)) 
  /Subject (\(unspecified\)) /Title (PNB CyberShield Prototype Guide) /Trapped /False
>>
endobj
19 0 obj
<<
/Count 12 /Kids [ 4 0 R 5 0 R 7 0 R 8 0 R 9 0 R 10 0 R 11 0 R 12 0 R 13 0 R 14 0 R 
  15 0 R 16 0 R ] /Type /Pages
>>
endobj
20 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 1984
>>
stream
GatUt>>lJ"'Z],*;s:L2%'&`^7gPoeV)A@PSNJsYK&%95Y+9[%l%e`TH?G7\G,WH9))-Q#Nm?`6XgF5tpm1<naV//#,PKSJaeWC@#:9m=CimRt7MQ_#.d7cd_'s:?Qdu><=n>`Ig;,[N%f^K!(s,.$JMf<3GZ+pgNIrn1\<ko"RtkYpH'CVC84,bWYTYF7K7Qf1LFCmrU:MLQ$5oCF>UaSBr&4&B#^N)PP/Fe=?kb:bE3:,j)8eC8\+qNYVC@#><L5r6Z7?[b&kY7)4?*?X@/@fj\G\,Vp&'CNc:?L(_>+PP3$8(l,9-U#7W6`M]fC5SNpU*0la=;$k#4@nAc4`/ekbsJc'An,h/"fP9P3<F]<@]BZUqi>lsIb]),Iu*f@/i5.A>PsKsIY9MB%KhR<J[h("lMs:#Ol3P3/%;Jk+uM9%L"Y"9%jU'T,toaeV6P#gIu\XWs&M5\1Ztf0T2_#cH"cKS%Fr*$iR7YT>(mP]SgSk<dS[W0;7`o0UTfT^/-7:5pUNZqC+AIs#iu^!^D#4I6u'oKdK\[G(+l2]N8s+)e@8cQB;CYDW>P=Z%E!2L@R0!#=%`,t^Knd^Ph*^3lrMqrt2RIm+-7=:MEm542VadX(<q/9_2L)B3c[a8NSu55XtmQ@?0pB";6N?_2',kBQu;4`-Kl+/d*-Bb@`l7#5OlZP9aO[TF]Y9i:>J*nmNW$>jRcdpZ1f_$+W'>h,%Ac#!@,>7KqXh9O(,LLp(qL>UFZWW+CLH=]%7XQ.,$jdFP_HPIhX'IaG,_FN&:TNMb=C!n7,g0)5s079aPNQn7C%JD7`V/C^Tk.!?)NQg6hfN:uZ=d]u/Ah>Ss5WFKbZPor,mtG5u(MYt]H)Yp(OnYC=DS<VMo."aWD7J?0?9I9TR7!^Q:;&BeD7Pbc>p:sJGmjC$/"OKl+(B8&@*o?n>%]e;a4]HK+J]G$_N-8k>\Xd[;$,]=LPK2E-XdhUX>1?_&.kcT5`h:_5jns]`]udcX9=2MA[]1SPL='Dm%"h`^9U3n'O&cf]joVTof<ZjRJ[&-4Wr6O5Y0Q!Fg,HsLs,='qIqs-4s(1:Cq\0q;aLM.clu[L!BV*6b[kp](7e<(5SB.aPR%PX\rMp9gf9lY^]C2]E:D3q;/?ckqeVL2+GFJoXe:6P9LEu`0^R<R<#?fil*]opTT=^K^o9uEUM($io@9jIZg5Rh3.NTMQU?m3l!U"k%4)Vf]&^^d'6($p&:MA_Ph@NR5mgJ?>(HikR1&YI>[RsC#/s2B.$Ig\$G/-?B9g/oJn0s4A/&4m#eaa!47tWH%:pcSTm_t1EtfK!:?LK/8&jY,2-IeAia=)i*(Z&j>MFh>WC*[R!`"O?QkG+@L.C^PW2h!H#R!c<"%ce9aE)5K:/<]CPXL->WB93$+gOu=9o:5u=X+aj/LQaQA%FaE3fsTJ+A93eoO+mn_4[W['kH)X$u[eR^E:Z#4KIG_;ds.1lL)1#JUnbS/>!\Ik)412?(iAHU_*oef!PmVkDiFC"U[9:Jcl=lEPBfX'%7_0&l9\^Z;bdn;T8]",7"0.SVf_EEbQbF(qAT[!,#?u*X9+Bh]>BU\o2m:m1onF6B.Ie!FapFPSJRSB=uDgR0-?C"4RYf8BW!GG6@qV+:or%,,)\9.p:LBV6a1q:5U?)=X+aj/SBan1$bBVSVVnQOD+.^7ta)6#GWTs-E>q*OKPGHDS2Pm*Y7B7T$TrB=`Rqnl;Do09%PfDiMfu4=X[tPJjp)f5oO`?BQtuMhWa$e@jnk&=:6`JlB<[`9X*2"F$U.QJQfknBpfA$Na1r#lU3@A\o#?.f]+.q`s!/Cfi5ABMnAh2g%:sL<ks\I;/bF3`ZZ?;c(9-^E6!.h!o<T/;mMKoM;5f8IShQ^4MDsW%c1Ju?4BBUk;Vad>n9D+GNk[\L\iS[*8Gp(ptZCV$tfq5HaEWI2lkVP_'"F)L#qd`AhrbgXSf]I:jj.[%#-85rLQ,OmjhH;#L=!mci~>endstream
endobj
21 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 1031
>>
stream
Gaua=h/_4'&;BTO'RQ*:4%6Pf8X;"3Bf#]2+b:G+Mu]bF-F-1b9HUu!a+UfC(M0HJ%q&W8dI-g2p/6]dUWm_k"R&Y>j(A^`_.3b7'+U5pn7`Mt36<#&5[l$B.Y(>=Pt]!<,MV!)1-okEJtOB$M.GNQbhbjgKc=@L.]X\^&_ZI/=k\VG)%e]h):4VdEN2p(/E(\mfn[E+f!t7E0]a!<V=q7</YNCo=8C!W<X(2-`RFmGR=#7'4.*[1--_7AoPa!%^!jH0WI7WH>s_oQ*rs%U#*kaQT_4!k?O4Y:dT@p:J1-G));JIb$m$>m<$DWYZ%1r]MW]%,N2-8`)i[BmLJl5"<>c\s?1/dMnTOgo+uDc5.%k%l"o`R*N)aXFIHK0\+h<Z+)>_`GAARQ[M7tPN<3q[Va40AjM-[kN4_MCk6_5"+mPj+("I?h<`UHiY#9i3<FH\\G:1*+rXW4=mo*+kcg^NX$LqZCfKAYK<JVrhHKM26=(bABZ-=46IDG?k4;,`HG@rGBZdl4CkMI:fKi6sN4.,lL#q'<<\-BtBj@iSHWh/T6W?pJ/V_!1T.?<B1<ZaF.n@`t6-CaO)kC]m'Ei@&Kk>3:L5<e<1O)kjT#2g&EYq;.CB-_%=7]o.\]4]5E2/Ke3#8d(eTZt8&ic'#i@m`1X_@q&pg@6<*6ijR9Q$<IbX4V[&K!+b!2#):.0,-O:Zcu;isS"%]*#pkYS.d;c>=^;sW?gIltYKC\l!&`8,cbn0lJT7ip%D.Vb^'EkO@[3m%ZJqF\3\Td2_KBu,X7L)*$et"5g.^JRprCPUJ>$;O&6`_RGSVBbQKX.UTRSi;*c0am.ppPl?7h$SnD"&s?>+/J?^,,8;hj!FL](:ubDc%fFrdk5E20H,CY,qFU[,_s\:R!7HEF;V0B!Fb2b$RNMlfN_b`_=k/P"OF@LI#nggGWa503__fI-%\h9$J?J[*>KY4*BXR8pE%FsGs9D)YEaS8QQNEed!XM.h;,?p5^&Kpf):I#4E0Q0k-3V7'<I')taC$_lO%-'?s~>endstream
endobj
22 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 2147
>>
stream
GauHM=``=U&:XAWfVaauWF,]O6*N!_40^U0jDZ<>IAS8lAk\=:%sp.^+5[6H65!ikjWp9SVKReZ^:gaZ5k2b9cfGAhEXq9a$lFcq*AEhi0`M,So.r_(J274Z9#5od#kN]`%V4n3`4YF?*^PAXNtKMT_')`rpZ;n1_@Ns&-VJl,5X^#QI`lI@>Y[BsL]Ef<..sDIo*nB25@).\h*P\Zqae[V\;eDc0$Q:.L"e.1dUK[cn@ji^$97/,=."Jmq4!#33>%5;+'g5N_ZbDpM^V<:(bW_e!T7=8[qTl<#:;kR`k;I'&>+8HEZifLhZETLrf"aYnUP]aiLG4ul!2Vb(W5V+T<h!+:Cn--J:Z#Kic/=ukE5\$Md7-(abZ14KIK)am\T'icFo/Ti-=YG:8e:rb;hDSHC_I;i+VkT?ZQLa_^;_ceLaVKo>_[FF96h^&9Y-50Oh*sKg(Wg@++3n'*V*D^uRkoNY;*j0$<0[]7"B9)&21W%Zt"h8a]5GE\!@-a;1%8C0@8Q0:#7rkAZo&K`u]GohYM_rA=EdEGsg0#4O9m>'k^h(d=.:aZunEd@8&d5&]X%'gWQ<,S2@<UEbl'K6B1N+i"O,N&'X*</B-q"VP>tLG9ks@+5KV&/PUrR,^75No[S?A9Fh`4P<NX106IYN%3Ro;6He^/B$l`/SlR`[p/KKPcWhlR]^-(T/HHV-7_o^0T+2c@@f][fa@:`SP5g>[g&8B3djt1U/nMNJZ]M`Xqj+OKLr[S)gm6S)FqtAjl@,IY/!88Z]Cu(:ZL^3n2/ubM51[m&^ia+ZDG/b?$hrJH"6&@m^jP>lf'.S#9Ka:p=5j?V-b7<+'!<QY4BEYkX9Kq'AY_l6c\9)PSm%CrIrA9#12<oJB8La@&'6#T(K:gC!ApW/CAAJKEkdY&a3-/;hPG.Y@%rtg$CLW7\Kjfrqc(?HcW\T;RO:tMOq&;b+E,.Pn$GHLYFjDO4\fUUE5V<*Td'SW^GGBFVE%'DN`$oN`NAPL8rAVOPcs3a9F-;dd.^GHNF!]VI-7S3\=*0IXtP_Wdm(G-5ttW5,.#p!YJ^,R9CBr%P[4R"@-d\I?)mZj>E5qLJ[./K?<84NoC"M>LegI7S!5s"';b,.OXeil01qS]M&]=A^L1bVN.KqDe:aemSTQgq?#\1319cean#7[O'D9^-[YjJj#4T\fa7:^4YZN+daN8ulf*^I]IGriFW<5H0X[ha6,@N9V.fB0Lm9#>-SOt)\aL6p9=4(^78o];E(KOs2]O8r7(T.gfl:.HrF0II[]'L`dEUHph,)KoB<ote7s<+O`ppW-SAVu))?.:Z][0(mD6n4snIEGjL0B0Pi]-rqHA,La@**=W&>L(q"Vg40e^&^/"B8lEkV2"@\eJ-_rY=N@?>e1:hK9*-/B8<t@j'tH5@=qPa+f*S^cq'<J7E9SA&"*GJCW/K#E_GX'YPp(q+b<UL/N9F(;=H:X2_"\m17I4ZY\bKkfGQRL_B.PD;D6_T5Q_"hVk?\`F9bhD@D5PLCJmE\D8FbZ7nZ,rj:3eSb9uVJn&K70r&",!]\e9M;EX3"hMZs"?S>i1>%js^J-h+BWIV'7ioTb$q2k*YfXAAI15]P6n,./ds&c[[e2V8Yo5t[/2j*GD612C:9p:J!9K4A<.I;e#,iErF7F:tiRFb8i\ZB2IXm&cQWpe:Z&+?a:tNn!%OR*R(oB$P1/7^<:#'@F;Q5r;r(iTq;5Oqb76?Lq?&/FCFQp+@68lt+@RJ_FK%4h>[j*tU&aN'J$ZR+Q1ZkAAp2R,?[D!d;2;2Y+Q=_AK164uk[&m$ZY[O<t4C%XW=J'4cf1&;V*1kuh,_!^Y(re$UIW*g>e]Il74K(jF]-jn&S:O)V(<!CkC)2+cH^`3+Y\,2dhQk6g?\\+-VjD74gI@WSS%]1&(9%(,0AZmkX5/B1A*gH/*2G79I?N>0ELXmn,\iNV8!4WVFp-QeSdMn14U#ZtXa#S%/KK&(gAKfqj9SoIXi]rt6Q]Q:3WUNJ@rcONiX!per,ZCCC<$ik\+L558!%6ZLV^s#%[amcMp&^fY5=&^!L:401?DUMWoXd=!>]iQGo,W;M_rq!Z8k,2Gct;()'n0N[&t1b$S67a^$lm#O^9]/lU2T1YXqo-GGU\jqKK1BKsUdZSJWeg~>endstream
endobj
23 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 2242
>>
stream
Gb!;eD0+Gi')q<+Z!TQTlU2$8!VSlnm(DuGVE$Nb>s;1$A20BAQ)*b]k'm4[.$5YF@RmQKZ(jl)#n-+;I3'q_+U/WfXSt/h"1T>elh:f)LX?g',SEQgi8*UU:_@]EJP`DX;*^Ms<XU<ncE_c%MA3l-%>kb?L#u2kR!sO>CZ,ZG2Ci"HE('>1?2U"*+@o6AMf]*G&5%p>0Y2o.iQ"T9ZPpI8HBu/<"GZNXRc_R0$t*2u<F2dC%XqTY'*k%JrD+8YJ^O3R966gFgKo2oI>Q#60s8qeMs#$sB=@m@"*g#B;d;#WdWjVOO9..9=j)@uM>rLldnaTr*pO#5TaBm]_-I=8qqW6pc[J)ocmVV1`$5J@1SVD,(jR*M,/f@k[#A*+=W"(a]X2!$KU:)T35,];E,%*iCHoFlZ(B6E.0q#efC(^f@BoFidCUPuhMK9kp^.K>--/,;dB)/GM%<8FAnb9RJ_0`ZIiF`\E?5o0q"MHPmSik!d#CkR=K\cUd]\$<I.5j(/*gAdkFZ!A+,nW0#M1S2(2:0kS=]cGWZk0[4Wo3n^L&$`!_!F&9[T=+hmORmREZd-N"T_Is!6Fj!EZcIQt;pf//s6!^Rf7;iEB1->!jR`L_I02=XfH+NM`K^UEPA+"U"[AUo#u)%1.j<Wu&YS7%sopG$#T+Y1MG:*>ZR6BnbUP/OgC5BA>CB+7t>3Pb=`'3"j[Eoq%.m3l'g^m9DOVYe`-8fIGU$*p".!J;^^T<D37_DmQ2@@Q"->pt-0I$lE;Z\5HWB6uD"8@D*%G`_TnPNDA3rC%#gUloGoobA?LE*Ifg9F6"1EF$kQ?+nWI1PI$>0Ou,->0$!Q?J^83B(Q1`8eR6GafaE<d7AR^I]Mnob'Du&B5X[RdD#]FP<FEL)p?You>S&4oa@g)MR(nW'8[/20*FE<aiJJ-8^#<U"]G/j_H9p:kR,4MUKuf_c-gca#HVR7)E:<d.Ud^a.^`-?sO8GO!Z_q.:99`NDMkPW9h_Y'e*qrh@h>Jk;RDGf.]\P48qKC1c!='PN/Z%>pEkA)[]5eY>f&18]BTS@l*nCZtN':8s3+*]E0S:FNVq%/A,nTKE,9CXNer-Q><?'1&KH>,1jS.;uQOkAam,9GO_mr"9M6#'O#JPV>Hj[cPQiAIB\t%)TP2<"K\rWmA:2Zb1(=P6_">4Z[+e@D1'Q>*HX*daRC#R2Pj;GHeR6d7Z)'l7nm`8m4U"lTa0J<g;$INPplZbVI%]Tf(BSghLZe$+_@,RgF7>Q9jpPi/I^=aI[;5J-YbrZA_#jCH##^/+5HXS(_r&XTOOW!KA=<OqS(IHt*lC*Ok;WA'`CAR#&Ej*Rulgh`QNl[9DIdH?0hlR5T2H#_(9j1^6d3bXfkRK1<1D3R/50*QN&Q)GIf(bfT'jOaX4j+p60'jPEhS^7&'V5DV_EHN'V3n3$s,1*t<E<R(%aWujflJ2OH<b4<>7G';`3!aj?_7KUni)GEe$:IOn^:bRL)Qn$I[H1[5XQ]8d5(>Pc^'jBC/'K[$@Knb$8rXc/,4'$E;&E8-;MbEE&,,qA<fP%h/`=`Ck?W+35[kL(Y(@7Vg/B'+fC39%*+aID^Y?JeqMAYI=uWd,i/WCNMP@(]WMD2;r0;p9_h8QBu3To;Z<OaX#.XklS[2Rb%pe&:!t=_K+Ib[N%r8A`hbWg0]f4JBaJ?A\7gaZp)Sg4.TmO@bGoi7R6'Q$n"H#=!0b/OV6m)LQhBSWUK9ISC],"CS)/FZ\aJ9[B?FXt:B=6>&olAu9/2^E_X')*pnm9u_RCU3$Bo]<j(38cX[r=f%l8P>R(guV`*ug,]-Al/0RsW@V.u<.^'R&l!?^]'g:(in&3`jB%I@C1iP1ajE1b#/DAMKi5-e\u3\3B9R8GQ:=2T@kpEe`ZQHK2.V=%47Z$^)/SmWr@/1TD%D"W!K<[efq(bLe&keCbT<3+JI[D'TFr7KsmG.X3F?U7"!*"4nU#8W2C/tt%mHW,%U+aX;H%.N*RD[)S,CJ!"r=7[SC&DF;?n`0"lB)H$k0;\4kmGVM\nmLrgMtmmto=7Dr!D9C-]Q\76\=.@7;q(@<24DEt=`1W\ohTf77Q5o<^ieHaj`cWnX5)b@KW$#rgM@`%8U$OjigWaZci^nS"Y-`.qA)=\A+"jm?-HOS'?$?hE:4S\n`]"Ljki45Qk`+82WC2Km[e33F,0Dj`/A^FYs?7hOcZj&p_JrU@Q.W"O'R!ujB/M[+A_"o_%uA>:uUd@OprYo~>endstream
endobj
24 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 2660
>>
stream
Gb!#^>?BQM&q9"Fe0?c-4+1&.[;U_'Q<eZ#YW"?Ko-2pE.*.QQ&hoo`5CQ8-9<5<$QmcS[T)eH6lDh"eYH#/["r';Gr*6<(hTk'(#6p.)C^!KF$*t"a5<C&g"Ipn`<%IB`5a\IV&s-HBV<2ACn-B(&4@U_8MF/H$lK9C^$U6VPR9<T)#=LH@ijZ!d6#tti5R"rN6E./:R'#?Bns?h)[[fqaoHoT]-!Vd*\]XJ#9].\Pb,jB9,5?C!0-fD>X.Nen'kT]!9[/E'm.&SLl.9ka^P$0gV-sFD_t4`&IfO+a]#"d&1(KN)KG95<4fp^U/b-"EY!*nHGVBo[64qMB#A\+4m^iV!8,k_e[IFr.!=p%BS.UhZ$8%>.1FDfT8BltAJVK$5R[9I'Xa(dANoQ+EX\b#>WTEJ!UV<:ATcbiV]_T>dY`g)'BC@L)MOlspj2VMr.7(.Y%%:?nhskl)eP=@_+E/!$a/;?<Q#N>OUWp,m4"*I@JnV</[EKGi"]oOdFtmhXn+ae+P/*EoM!&ajQWqO3E11moXq`G[kj_IHs7PVITGRa$Vl9.ak==k-r.ZF[UP.m)>)\*C*)]D;3!MoM#6Y>I$H57:ZkR3A-:"@.)$gX1/RX/H#6kG8\rjmtNtO,H'll_EiIVAC4D!5m;U:_RFq_\:LI,62M-hq*1.S5'd</]Y\M8GeNi5L_N3D7SZ-\l0_";M..DpE3MsNXMiE`l%j0Udsl1C]kdohp%nL@juAVA/#jVti]`Oeng9U@HX<ol]98)u*`8qm:aXZeA"H^,[Ac]?)G:O5i_*`:YGnR.-1%^.EV0uG`Q./0Qn^Em2a]jk4!Z%Vig36SU<*p.FQW"R[qk^4(-SmX47?*0Dig']!EmA';jEnoLpc\/-@IU;i=H26<d?6&C#SY&STqf8?o8:)u%b!/NYIX>.^=k^GqihAM@@9<q++T,<^`Bo+3_KFFM5MW(^!]nFU^*?d3P(tbr[`$`t$/oB>Y+hmribreI>h2%+oPfQo>@7k^1aeZ$"`Mod[#*34f%CZl8=:Y"_dlt>&Aiq"/ke#+;-O1_a#.Jg::/&dEWg562EWTRj%U=ug93FK(E^*@(qKj?"O^KA4H6Vl_$#Y8>#eS-W0@Z+GubV+3S2A6b+iO3Rldb.RJ*#.O.\*A6rIg3O&6hWW%R^_J#AAiG1_a`kS7KH*;GQrnFH2(S(Yap$XKYM>h9l=@GrC/1X)3:Ia/Z)6>qOuo8+*G[dX7KA@Z9QM`q_shl[7&<ehpI)F`Lo%r%2\9h[j)+bkK`D\pm[+Nr_[qSf<jkK]VB:39FOF\l'tX:nS[2l3%O[CiMWCKiHlbGqRdm90n-?dmlIhN3;F["E$"-jNQaO:EBb^`@s7!#)__7g4)QXU]t8MMJQHR^'[M`M7Ul[l,\aE4nis#4SWa*Q,!O]+ks-n1k`;2lkZim=k9.'W.MU*V2s'Tq@rZ]k1UHr4MpYF?i(.keW74=)EjUQK+EtDDcXSh;!Ok"*9fRNEhL;.t&!dEbDn;[lN6[G/SFV1J8nDCW%u"-t]\A(Og[$D.l[LE*'1PE3CBkAS-[$!8hFKfW2NlmBpgpB[;-o[JSd4KrSm'.Y?6\<Omcs)4#KTI_.sjUeC.+`tPY<Nci<BN4.:,?dTWA,29B6n=Ie#a64L"d@OmN"ffEU-=i7@2ds;"IbU627Lk4M(g:@<M*Q9is(aHHe'4a3L-9c@r'rIQp)dVfn_nk-%H8MJA/N9.$Bo,CNdo"!2qAgoBUBg8fRfeFl]s24'&,n#"c%piME**TX,:$F_6KQ%b[[--*Vatuo`Qn&GJjeHnQseV_hM;ML.YH2@^FLokOe?#M,aom1M.%Q(bQ]tFj$.rdJ]u&c)30TbaMBcTmbMi4'KXJl[Fr.KK#[iTcD,2rZ]YJoX[iWVnCJUB-`u=W$?#L%\h5cRqojF=/?p[mPjBZl8Z\9WAB9$fO@[R3Y-YW4m>>Dm<9[9GaL[)W.M]g^B$Dl=*`G:r*Im'NFEQ]NB1i"jXcHcgoK2i(^D,EcR>7WKEp#g:Lku:$P1^!'NH.L@!<q.U<a[3.\_53VE4RT_g$[Kk)LDCcPS^JJ5G-LBH$",rG@1>%b#'TUTe\)f1*$#O4slB%?l_:Tc^?O)5bY,VAQ(6)oW^*Ba",)@5V\^P/FZlF_dJ?P1(BD7*575[Q$JS@t'M?m73ko?amj3i38P0O5Ln*FP,nCS*qBkFp!(Y"t"'pPWNRA*4SF\c@K2-k8^u8G0YYC^n(X$<ccf]"1K(I4cV[r@8MZ%(Hl#]3k,XU?<CH'YE$1$mk/qK_4kS:_5Psl[.rQ>[.%dPfYn*ATnR+aI-We7pN.#p0J0%/bdZa/n54;*"_LB-78FW[:(tqjU31Q5oCe&)Q5sQ@[Sm=SP'CsS7KK9e\S((kWh&PpimbV!;:Z9W]D!.Gq+n)c5$-g#YdIbCn!Me0Y?UEL-h';OUYI7t4]q[]3$Qu8"Ic*n9faZn0YJcPqYO'jo'N4)38NAT#:tE2qE)2Q%(Y?(<qER(M"C2j.Ol5n;1[`(-fu;=H*j*^`@WXY1-B)i8F#^c,RI^EpMoippI[li5.-3QoE9',/L42>?/@DQ(Zlk8Uj?>R`?OW],P(ueQ2D,PnHL"45IboE%dT;]_'6OQ84.UfJ"eVM3pq[mA8l[1oRHb0q?m~>endstream
endobj
25 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 2544
>>
stream
Gb!;f968iI'#+6EoMM$^?iVH<E,LN'LUWGJ@V]^2\\KC?1Qb3\8_N.(q=2q,7"DX8q%7qQ2QFim)X,f)h<9U<JDuL;mu''=]/cC/@)+bGYCZMfL\YS-5<g@AM`;A8W"_?&J?V:0iBa_29'a_f'G)Mq#T08j'-%>gf=r=L07;`a*G9('7mu_=ijWa%K$R$(+qXh`$)O=(@D7K<m-?_m]t`"7j\;IN1!E[u]$?0j9OUt4<E@r=)Er&%=9GI+]RfkhR/aV8RM3Ni6e7b!LUr)@W_0QrXl,aBIffNWE13WTa=s_/[;%Fl5XHA[aalu)5=KP]nVG(gm/cGX_Dr'5m9F)7>J]FKs,J"7!^T5m,6f<(,iG@]cQi5t(C(q-abZ1DKPAfCQe"9iHPrr:j#curTb?1fQ*YDKG!!%(i#29ZI,GPrAs:F6q\`5Fjc=?TEWSR"&9X"!ZPCpnhQ[h*CK:ZAYN'Eh[OcP)B1]YTDKTq`.)QET,.WfTbU;+r<n@t$9\5Cc3Qou'8Z2#VWT-J'jK#HOZJm6Z;0eb/b8rP?KE$E@%KqY$@"G%0o\U^W&VRb1#oP$_7`L`(]h'@jr.^7%&T-QZ6ir'OS4(g"d+c2-n-/TLL[c]SR,Z">ir]U.-\nr<-"-WW9GJWTpQubCLHN1[)Y@GEC/\]m[E;.@DD[`V6I"M#R8fPof3)/97?U]5?%[a=7cehB2cnapjY<:On1Dh+$@,ZOpfXFJ$G*UCj]P`'$@Rk,bC$/SFUY:g<Ien.Tb^XKX'o/0r.Z1Xe/.ljXU``\*Z.;Y(8A3d%q6u>J-[%Z@;4ttV&LLT/9MALb<nM0T0>G:\`[I;dtP8/nPaT9<<a8/'Rf++ICW2=@-T^7YQhQ.GRE"=AGu\4lb&do>/M1(N50f#D2TQJ"oNB1))8'u0=<8F2fPT#pcd)98WFriYK.GZ>`to?hcOD-NX,3SFF=$IJP3])M[Bo\-Yj/I>pNSN].$RKZ;#mY(W)TOa.FF/I>F=&B^4iZXKqLTX9bWbXQWO3Wj^I-Bg->f9KWBSX(:`6C-CjdWV9)T(tj>pn<so4S0hs%a'GN7aAlB3PVIHlbFV$RZ8>QQ=fQS;T4=`0j+HG,pet00:+!98R_::7+&/26Tu]0+Q\N,J\q)\rF]hqDj/"B#UV.b/YC/[o6Jj-dY#`;'#)cN!!EMd7[F.2aE**"Bnf:)[PWtdMLW@HE6P0$f`6@)>f*[G^,28Id:h"nB%/GG2`5cimd#e9r>!C\Eo-mi!^]dp5rJddi<KX6AZf2?S-mffNXL\FT$\#MM5/[fj"tJsT=.=>9%ThNL2#"ZPBtB[!#LR7VkBPQABW(/RId`^q)?n-Q^mVoiZ[A9_^K$?&2NRIs\*;#jO$I%nls'?j@NU0oB]/7j@N,PH(ehQk]r5>17tMjm0+lD08HS72GCmSCQ+#DsBpZI[)/\L7o3+:]$D^UPqh3GF>//=<':8,fSaO>sNYk,6`WT_aFj5UmZdgWSljYk0WPX9.&*n73`U9lmO3nP]o-E9GYT>lu_:pq%FD4Cg[(G=JX2[tkEC#24m^_V1G3bdYRfN+H^$^n%2ouZ]ng0;k0!==rhn,EDd"_KTL)u9Y-@m-1r2HmXD4ViegY)BWI)PI4:>I"EXqmhpTD"Qls+iD(-mXB4r8UON(Ial0_d46K)oa(lKl+PpB%RPd9:`*b4VYN=%9?&'[IUH5X2e*:#c\&mpqGnmac28./nrs*A#NgP'p02*%DX$Z9X5@A?/`k5gm$fO<88f.h/SS3f&NJZW[7Lm;Wf7QLp_Z\U(.!5S>tsb49ulp"jS;"[DLt"D@fV%MiNu1DM-7pqI4,\Nk<U!^0hj&koqsM=\!m2MR(*U;7e'K]Ac(HNDZ)\n_N_bAgSNu+2<$"K^2gNf_2>IlI=\!G6L=omK,dGVD6%2bhRj#(EoTb#r,0=g,3'rdG0T2CTiK>rL1/1[[%=U1/2VTjL7[m9B%N9m?4CmaUUa#6J%Tj$=+*E$?YB6nVi6-E"1Ja1e%r2(jT@!&Vb[PGk%_:n>jHb\OYO`HGZL^k;]qYgo02*V7E@5dXR\qG-nK?e-AI$rA@@f/KS=O?Gb<DS8Z/:cP\=uZTJ)@U-.=KlHNJ@?0tPaYi@_2LER%4+ug9i7iZ;jdhFG)gb)Q7ATnsWan@l+$42'9Ce!_tcEP%3W(VK6el)iJ]KeA]:N^5$..OA^Xij>;;Kqdf$=da]:(Iq?=R<5mcHVmfl3ZqZ>26&uWQdU&GoA'Q*DE$+_gm`?Ar*]hhf*\`E>L_XqC=GE@>(tW6h*'1Hf=9C)hr9qT)J?@)lK)O>e1%p]iV8XC=?LgAIg6KJS1Z4^Y)bj!Ve]KLZ'1>Xa^AcE@-ZPJ8^B)54jYA%_d(/Q)o'lHC^>=k`):d^OY/hZe-%d#/0EBj/0'kolZ!/Bi6Ffn>SP7`NHi>5j&#P5W?hJ7T^M[]Yb>h206/s0:TLsk:[1r6Vl%#)RO*/]<J\RJC/7\ZD>1uWM/ZQ:CU`NH>3_4do/W<i].h0J2(U3cr/br>H$iSbsOkU:02E,%t),`ZN~>endstream
endobj
26 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 2709
>>
stream
Gb"/)?$G!n&q0MXW42HFL7\BFlOdW&P+?jg!H[hq,D0e_!CS3l?-_+F^XWCbeHftYjG\/'_hi5-V63_P>HQX30qe;Mjj3H*i+rP2rl0J.(u51U7)J..>`;D`'d73.#W8%U$4'SaBE?fRah0`=Ko2NhK49LSTfHX<h#)2EA)R[K2Bs/&E(KV5>l9n);NRCs(?uH55U[(8!2CF%Ie_q3#-7&L)r;n2F93P];/qe31[)Z1/1o:Z[><f717?(r.G'')d2*YudMePfc.Ma:bP@Lg)ZGPM,b7G(3/cp+!WE0T8EVoki4MUTBk'C8,bW9s%`Cp9.tg^%:H89QXFLnOE)%.l>Uet,VD(..G#DnH1smHW)$HHA`<2*b8+RrO<ZIoD`0en::K?MQjd<3`N0_9L9mL#@KB67VBj\mVFB2=+f^et:)i)cLFugUKHiU/bp%X=b(Ef@R;<LK=FdONFDJ3;bbt92LP$b,>ZhKf5#8ToC_mQc$p;@?S9.e'27+UZXfkOB[[op)J9?(q:9W+!/<,k\eUE[tpnU*hRs2=qE*[UkUjD09Z$2MWD.oF-[2$-5R1SMK%cX+#>f!;S+0>]RW8>n6knfoth@$N[`O;_XXOCq$J%hB02"WGT3%V#N/5i-3k&IF*u-3E^6ES#iCZFH[A(bC]/bjVfZdO^5rM!sA?"_4b(dI\36`SKkqN8q!1DNZ_TrY9g?=0Ea8:LK\Dmc"YLEL,`IhurPY*2:D]CAkA8CVU^"L/YoF8RK:X9CJ'91;AP?,YtS,Bi;#dOWoKtb@k35B>#k<^I%ke7@Gm9QokMVeG'Qt&E))[AK_fuLs(B7#d.3cBVW#Pjb=&?nRP?sAcMIGS8;7jM%6si!_coNUk:[l%N5JPk[<b1KN-!T85"XP'7.*8fBk,r)it<W*h3K!0q,m,$`[t9HqUNhYr8*(&oRp&"qL"=!T#H;A'9a_V@hIB5aXV%-nTC=mk5He9>L.4Thil:HP9<$!,H@!:i_)b%10891KS$JZ=Kod;1DBTYGq,/GdN7Zk#?3t=g;')LLEu`3"Ggo;W.1'>\<a#.\=-q4KfQ^5A,jEJOT?:nINSL_]P^Ukj\&%MrYpt89fc$FMI#1imAQI&10,oT+ue"Ii/$F"HC3hj6/"peXjt"F*[<690mDe5>g_SKNQV?"*`Ak%GbM9&1q-lg[ahlc^/Y.A7*79`F?S`;Q>g^n^u9Sc67-:(.3Ed=?r[o<;:f=f^3G%H83DY$bbHX'tfIf\&BAX-[Ch#f?:&XDW+[#>#71C/I>W'7VQAgJnp7Gm=K@Q^!l)*:=,&_.utR7ml]ib%PnVJN-DD7RDd*R(iRZ8#>@j.hkL?LW,]Y2j?=p!,)BU!Wies\o>64SN30<XgUWX@UFnPL1?>O"ECEhXo>]lMXh/0XH.Z;Dcb1Sl6<@0"Pfqp+;D`;;%K$-nGERk.6-*dT)Cm8_YTJEKOpF'FRaSF7_Pal<[tFZAkeZ@904;?+Q2Mt_A2]>n#qk>;X#`uTe/a(]mK)?IR\KlK,SqOVI5#&7,S;N#UoXU_O2pdbLp!Y\h)(ZlF-n6ZR@Vj$8FatIn:*F9]Q89>`k+abAoJGnS`CuVU-XbU@kJ/8Z6-A)ZG<b]D/.-uVs+?#qH.T@`Aue3nScM;d]DXIEAhSVei7eRO*(pLnj=MN@bp(@&&tZ&,`KO-].%`%AEj"-!W*Rl;k+'TPB[-fBa/iFc]`Aq)Wc8"=GlqW*2H-+h+4T>AknQB_l!41%GR?$3At.9$tMJYE<beJZnk8!+J"(1#$r0Dfrh;_c1QY2JLRopXVB(26"SrSR&)8KSGO&-'[GZa(%YhH@6IjB71=\.d;Afk=;F4c/cPdho$`hu_=b+-[9.<Uik!G,Bn=/*-UGP"@rs6AKsRdil]t^lg=ei4ranKM7g'80iAg5IC)2]Ib:G*4qXX%",aTf'+V3nM?OY6;>kC2hqn<!JO=T.64h0hfht2VbF^G%rqdJ\V60"2=G>L6P0PkV142ZMH]#_]Y_R4>BQ$3U+9$d?-)HeJ?Y$3=5cNeI\:YLk.-c4QW8K<Ud(HHjj:0m'KXb^CONRN>mI)l3<F<Zi1CtQQee3sju-<u6^2Ju7LAin?!H$$:/ePYPaB_61eKi?gXkI73F=6CC;X23KI$A!4RS`g#<#B^"Za*Vi'J^hK6q>CEodfFYATgI9@ID4qFNfs0"?=^<h_XF)5q2YKmig4`"`o!6N".'*Ki>S98?6)-XIKdcK>8Y%Tr!M^/^/t5mdREu!D=\eRoU!OfID<\6rin]leo/=6d8n6:)c<-3V^5@mhYN51h;VH'FF!4Ub2_OQSLt02>CEa.PCg$cn9S$2?.PV9dTuo(5pU$^"Lf?IJI/C.hQ[a]HaMrR*Y>rIH;*[UB[.?JVQb8a4_lQ#/f*ilVdn]nS>A3oosUcfeU>V^.5q'hO9qrVp1:.89#g+3&^=DN[nFd5g^e`J=YYWT,=Rkt\^u.nGY\M^pAHi3-l9u6XbcM3Q%sk3I^X?mBK;c;Wqg_-ga739Cu1Nup1Mg;h6X&<XL;515%6O,73.4hC3\!t7jX_p^Rmi`eB)qL)SEh4J,\;)aZMn_DUsePb*kQhMtq8]G]"$c6(N(pgkn:1#("r9csK86Ve^83^%-!J'Y+/mZr>nj?c-CJ0\S=iA9MNtam@/HbO"f)Z)(g<LKki:Vo%,U&o/5r3N11He8%aZ\NV]A%1Xcc"^r=..f~>endstream
endobj
27 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 2325
>>
stream
Gb!;eD/\0"%fW&,_(Q%h$[XYt)XSOT8@-uepY$gn]so`m7Bn5F>$5lW3B73=j-QOMO_cOBH>_-[Bk!JTP!_Fon?Eg,I'N8:C^KTO$>7+/?lZ%&^a,$rI05hb'1,./R0H!;k(*TNPVu]1IX@6D2lfae'PL=%:bFS[gqq<3-`@D[\?+7tSDoXo=tb?IC)8-CMM4(o((a(?'>S\rVcW=n_Su6&k*&5MP;uko;/qf]9,PQHSeYD5?!2E[M<>X6jn]-S5Jm&j4k6'9`cb@#dZ;d5]ShY,9;;Vr7d2:N^AomloEH&-73!ToKbR'CPqa87On^P^&$J_fgm8U,65.YDJu&uHqcNuaPKtV92bF`(nrNn;+GpCB,ELh;KNK1TL(Ro^"(T!B_FmOm5.li?M;r`']hnme<-IuE;;KN$-jUW\ZX5_G?J4RRH?f\$)rUJcncf.f0^B_JV_ljs]N;3SeZ8lT0Ca12Q*#rRDCE,JX7mE_-A3#ME83OMO5<KGY_BH%%?B=aU9rQ()fqnnq0#bK[s>>aCtfIbfOu>(G.g)teaN;5j28*oLkdm*Zin8CSR&4f/f5U$_G'1%err#rV57neLmG83#737+7FZu[$76_!8.@<gLd!%kN#,8X$OUXU&B4dYJ8!G73"cK59E\fXd%%OqY*>qAd*m\k.>9+dbA=ma/4Ag3F[*+OmU;C8<Kp^hD63DD[7]F]=d!QVSD.0V"_q2NP^T]4"u_N3D2Mp3Wf(f(EI&!NROq/!"oa8",VJEh-:O0EUO57W2tf.uD+B+;0ClV<6OA#dYu9UHgjFX!k/nuNF:qf4q;IPFCir57VN`#DUrJmh;2tMFj0RbqoMH`MPnKb]=s40CgbL\lg46uKk(E`TO@TV,^&3ps.9EA5C9CFT&GhR\!*;kWE%9C&RW+>bU:k$fd.Bb`VZM","1LA-ZX_UsCp7P5Q3/>1DCq2O(cs.WMV`Y4HHZ"95YR.;'2ioS,OBqW,(Z[2$5hHm%l@TQ82M/t5Gu2UWF+7[Z*.aU=fqV4,!aNDL&f&GjrOOt(MM(fjZe.X3E&<Qh#;@h4o9]I0-j#@\!F)'mh=TBrpYa\>S&70O_9l&&J1^bif0"H:N5s5F0#r8m5@HsS?Gu\r&3srqVeb6"a)F\UU''MAEf"J"?uH@ammi`HW=Doq/GbV_+s^sZ`*i=M,FN*c&R,qV-fnn!gc?b%?)EI=Xs>R7s6h][,kl3_ti)tFAYcaoh5k!nn;nOOeEe5.i!K&)_OI9dLNfV.^AU$5tS9k0)7gkkV)7e?_`r0]]f`&L.pk5Q@+L=1JX$gYo;A.)Z4='Q0jp'WL3K_fL/Pi7YH5B.Q6V\khM<gR:VNpMBRAYfanBECcJ0<`bcbeXl7!As(_\kYX.W(c%ZZ6!osHkjmuW3q%*2j-:WUPGMZPIW/o&uZ0+CS_jZ7Fc)f5pfU!5"$njrA(nLi8G%7.0obS%2i#'2d*5n[/%5+Mr-GYES_>32'r9E;/#VIcZq<`2*1Rf3\k#@c]r&0s<I.-O[5E)),pkffcP\NhRD3i11QN%WH%-$BscJo2VVPqG"pTJee!EdGg3+b]06_&XR:%qdf?Ts:JA%7+9!3(1s?I!1>].0Q@`-,i]B>l"'No:C*K^j!d>^Q[Hm'aj\pc:#sYftZeZA!F`BB_"limkp.S`-<@@i/TD$(`=t@&dp@mQfF_W#IBkH$3he2D':jHV4n-MBB_X::O.q]@p[u4lIN\No:2?NmtP*qQGlBq=O;iK4m<#)b>)Ed6u:t@3`9PT,QpXpqf=J98B]':O3_:Nfl@jE+!I4oYFSaaW5d)hSIfJH`0:P"\:U&2F)":>Sg"=4PZNg&sr0"WuZJVY3g%hgMSQ'o&8G)H*V@K9+loPa`1muF^`pBCtY"2E6$;m6j]I5T@89iIi9H',gGaU\D&:.c(jSAVh`oJ)HG,W"-)RO@<=pc>'R_u%_nXp3lu!+cJiu47,?7f\,Jr%Xnckkd>?.Y(O+Qo@QVnG4@SiL4%fblR@_?AJaNiO(W`15H3*I@GU(SJK!LRun%As"kRq2JM6,T].5%b9keujW,9J1t;S''npb97Cgb8GPalR;f;W1/,b7GLMM3JO"L?W:8#SfKm*eR7aD_44iC0!NI7**p:*5`l!>K<h<aIjS-iBAk0jYO!Wp,\8tmL`KXf&k7d7to@J`)2J";T8&gmceulR*6Qsp4'D;PhoU=oCUl)ag?/;?-dbF^3G7e3rDGJSsPXZP/,:+DiJCk`7K:!A!:r<G9(*t^`B#.>s(6dD8j8HgV;B&Rq+%b5[oQ>+E2[XRgj8Q7JL_YgShVk(<r2nC;===q&:*j=/#~>endstream
endobj
28 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 2237
>>
stream
Gau0ED0+Gi%/ui*JWErPAk@ku>'ISoHYosuXHtj%[s_+a,uH0sW?esrh1#8eaWa0sEaGcsQ_Y6B!5e=-"AB"65HOgSXoVi\iV?[^N5P2nQllHrBCKMY6>.'SVLVL<\<]CI<(9;Q?(YreLLi"C$5?$#.$#'t.YFd7-`@D;\88(r=N*!l42#m*m9C3m8/A6CQmS&4ULC]fe+4*Ri:Yo;<aFMA=g<SM,&+4&C(1P1YKE_YmVXh*\'7tlE6?]aYl"pQB-Yrs.)ts\D`=;P9DFT*H+?KRGa3*Z!;m)k]%gPa_G-4A`BYRMU8]u("#0lW(W3.p-QKk0&MT=kS5T`0*t!4qJ;]Vp-bVH:&Jao)J`_n^XqaDI`V5$fEY*s;@q#NJfnYp&3dl5jD1U`Zn9Ui6_pd9V^IIrWF&[s3Gb2\3&:7ud(X"c#5kQ6@+7\A#BM&hYNhkp`%"\/Q<Nhk!7,TZ3:0W8-'*>GLShq##L`!:RIE)T,#ek=pc4RXah<CD'P?#(l?>"5>V;!J<mWtq3(MR#`#CQ:[Im+sP!(H5p7'm-rj5)jg]h8j[-t+I20+uA'jAAhIEb%Yp0nI7MN?U`!,9i(fcO9t$Nf[s%6>!1:1';G<Cn2_]/.(k.J-[tDktstf(:"Fe89p2X0Hk!(hTHY(C+8+%R\[;$jW[qa6C21I"@lemk_;?CCXdCeXCI<qV@a92n=N0LcrVjI>=>sARr!*DnTAWY"1>,Nbr&D#LE"O^]%J,0H;?C"c#u?^N7U8SG\*Rl%-[0/i&:8o"tR].-5iS_4rR#3Lb`iKpBrO:'T4CB<3Cqn^B-'f)<".m6LmFJGGtkk4KIbhKQLaibWO+T%0hu)5Zc1V]mZV,V?`ICP6U<$^#CJeq8%h-S6i]7*3G$PMCn68)Em&kCpGb)4:5XE:`)'C$I,2NQ!rniZK7pjg/^Nkb*Y06Gdq:#4>m=@5CS3(/r3O@GQ5t`=`Tq@]lt%qa0ifQ7)q'/Jm$m:1h0GMbaqm]g"(qFWGN!4"6$PJ!t)B@-U6)$,2BgGp)*pq^fJirjGW4\-8PpY,g,<No`]uVSG>\YCSoLO`LduKMl>gV*uHP9c9pPI'BX6:bDVBia,R==\$QPZ9_2a(B-\eU!'&!rQ/nD=IpTp-L?)M!.BL]ehB7f*0=(p+3kugl8!l-9Q6C`;>VsQ7PuK7UXC0^<L$!=\'3Ao.-mU3H"=+>mdj1C$'hUGt:/@T]=@2g?LM$'Fim(+9LYf4QX7BI!f2]-1-:MqK!`jT;>S\1kfl`J7_6"`#d^#g,Kj^S5!2K<O0pA&[N/HPpok>8Q_4kX-oaZt`L:*g5m6$g1+&7=+*W>LSBpQh.6t,QE[]@*'"O_!:c/OT"*C2Y;IEL-o.W7g\lr:]:o.!tXJF0K#<efonTPfqbMg%%'r(pu$E>Kj99PNR$oGVr+4S>KB,*X1K82Ib"8L48+p(-kqhMjdDU`.JX)C%rQ*UWg&[Y)\0Rh+RMMU;j8(u1R7[A`+]#"dPNr<ATWR=9^mK"N]D/#]f>>Fl=p%5a#5.:RIQP_nd8JF0b8VqQ]Z7(\;u%L%JfaBh&DVXb**%oktc-BK&t:k:lWJHuCq$[<fP]mru:&_2cpL%g/;]OObgmk;>DCYcgAjmJk0:JQWW8*<Dk3B7t7fJ!$Iam^:ZJA4=>!Oc@^:'aAP_u>!86.Nm>pTpLhT'Pk_V[b>iB8dMulfAA<4CZ`;O.JS?VQe-#8/PKr<hX23"0cNTc1D[.@a/OT`,')95rm^7"q/H.`!Jl"eFEpC,o/Bc=C5pL$Z!2bW<oCcWD/Bb@ID1kQ^9-mbI%k-+J')?*3KQURlCWU)`0@EBGuI_gouLL-jN@(EJD?&e7`=<'kJGMeS61iJTr)s3F'D9EoE3L%Nl''du_f4"_L*&WIn`b^C6r'VeM(Vp(_pFd_.ID`(/6d#"/k3auDcnJ-:HK3AL[XS1*>pACSJNngF)q-9+4DHQ>q-Y2DAa[r/G0YSn5^7VtmR(puB;^pQ1mWt*mm:$F=$V+ArclrNI*bWSZo'Ph.\+#bqQQctS&DSa"V,%>dB+s)4ZJoQ2YB*K_XSPn-a9?We5L50!c6c5e&ek)"Ufa=/\&m-O]k3MCQb,b6OKY[HhP3_E@;ng@gW7rX,]CDo&nP<"I;V,&MrsIYir;(#MA9OF0BF2dm"h370,#9"V8SS]Y&&HtKVgFURht#b:R[[gi\NLA-a.KuP^*\n&'T!$l?Z"^ab]*,;&k\PD~>endstream
endobj
29 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 2770
>>
stream
Gb!#^?Z4[Y&qA6*R&<Ar@5B/t;,eSHBUtrcgSUIk7W0CB7Bu)ZXXn$p3N7T,n2HR_;2V4&DA6Jg[';acr;4_ILVkg=pgX(!dj;g,$(P9U?lUM7@"JZOI"]\b$)*C*R05jAjIQa4\Pc!(def4fs0Ct&":5]G7OWI+LK)1h[hIhV03ksIX:/U2a=UcsP\jD3S@He04tr$ol7!5j9/sW`oH$Jk4.VBJToN`()[4nW8XD,agGI$8D"F=Y_`F<%i0;Dl@IajS^[88f6o+J+ofE'fgqfm2$^3Q+i-c/d#P]CV.#I-.0[@NXW\L;74R+E8JLH*<I/*9kKYpaV!Tckh3H\bE>u?"c_>**[P>W?$''XJ0J]AXJ\L5er8D`B9Q\/+n.-2rr\tsafcI9@kd2Y-[FfuO[com)Q>r.AAZRQY/j.<S-%_cLt3hBU5!`_+-I)_Kfi),*)Et"L(9HAB$>*c6m*XFlhYL>0$+\B!o^@1.N\.2A@.Uul3^;1OY6aeNV.N?*=L;N3:%m=32iM.I0Ge28.FeiZHf[F3cO*GoCQU*`L;<:%;n(Z#o5S=#'-CP&:q3`\7[nREp;8SQ9ltOhi"HlZIFGp^EL^)j3'T,cI/)d/)\'Z?E#iEI3;[s6+iQ14JK%e@UbX2[RI1d2^!9"E/4D+o?_W<YPDN<dgTqOddQAKT7,kJQA=-,"3Xj(L)FUf,p0FLp>]-Kp[/&9)X8-^qU]a,]p!(!j7P%Ba*TUP*N^R]6HJ7)O4i*OGbbu5OP_JB8E8H/ta:^^2ZJddeI6X,\>n.cRccj(V\c<Z(+;o:Qgp5@!af-O>*431HEVkP,k;_38(4j?.KibsC/<:+q#<iNuPBka,d@iX6k5ZQ3OfjV1G[1$!V(*/)+=\Uhjr;%&(X@moW<Jn4<2>B5FD99U+/WiG.W^L\m:'fW%\7]&0K2^gWd\"D]Budj0Tu>tXr/=GoG=/J0>G2jZ2,1tN7P!/O't^<ia'F?QoeWm6mdQ5NC+K33:Q[,_L/%6!A-nheY%icuBW.@0PdhbdmC.4HB2]X*<d%sqO"=j9[V3W"P9jcgr&_Pu$mY_L,P_62)U$_`>YPl1IUJVGj(n]oe"_FB4RkS#Ut&(M&B9d`6mPm08eX;l2bC8c3dUhHblDWGO5M0aAa@hMS&.K8r2sG.!:Ri&NnIp"c-#6lHZ<&"d3Q,m0DOkp1S7KETl1><0)CQmh<6r+#P<H(;[bOl<U3r$q`q^X!,aHr+H/3k:Ki7g?cs_?(=<=e>72QH!&p]-Jg;pBn-,f^Hkeaf]8%M5=9GP<*lm(EHS98LKK!<]^n2^hIh#jCrb=<*XD3TBZ5\.U.ZuJ<9>B,=]HmXE/%[%aaK0%a!(f<7gAq"F1_gpUN=G;D7PVt[*au_(JiH-Uo4DLD?=BXoXbO*T%%,HK"0tEi^MfU(R_p#Z`8;L8^%hPK+](!g6u?-SjdT!HpNb4BjXh,pHR@31e@K,\BY(+%G1h%AG%#5Z#:$u,_RBZL[P\+MPltnPC'8o6#RpI?4Go)rlG8?uPZpC\kg`$ln*C<cl<uDYXKs2eat@pU:\];JL#;P-DKM2!dfULVLHC9*P%-$,h@>[)ehqeX7)fbq9Rhf'g<[:bWdSNarI!@:3i8kk0-7=OH9=\1j];9(#clU+@dDFG6%5N44^Kg[GKdmqZCT8Cco/9@C<M1c_b,`9pCi,^VNOaFN)L#])FWmp,MsWPm:j4oVUiY$WnNncGrp7Jp5HGRXfm&epSC?k@PMYPkGbR"$e^dph$2dt!ui06]EW>']7OBt]Y9jMT2`rj=har5+9'.;Pp\+nSFM/LC&R[(,I]QTs#AC%cq'S((Fq4"*C\(r#.\1YVrjEaE9]e6+\hL-E+7)mpNm9HKA$BjlJohBi0MKcHBt28^''EbZ*C)DU->sS-/m:U&GhIm[@omMfF:OsMK%E;jrFk=&u'.Y^:F.rePV!4;&dH$%oT\DPn`b9dEJNSnk<k"WNUX,<8W<p*f?[-XRZ'1N&7+\k2@#`7@R3"FksS#Tp+uj.D*Gk%6VaK68aR98+;!H9RS<74ee<R@7o\8;h2!u-s8_Z1$W>4C+emCWXlL\CEI3UnClJe>L=ftI41n[jmP6u^kI4GVmU&5#8Y-^g5'>r3<SB#,Ef$m4sn#JZP1'!%qA2E9eT]A8(9W0e$&)Y9J=U186Z:T_qMc4.!8dnrTG4UBTUL7J><D[)QJK3K8(9hF-s(n7#f-S,[M_C-AbohC/C-@1l\K6d+"_c5Z<+X^13s9EHGGd5b*llb(l/:3RY^,09MjH4%C4E[gQM(dO5@<j[<Saj%M\Qh'W0X4k-EPnRP"R6\:[3)o^PVH%'$^A@1+n#^ct#_g=0Wb`^]!kJ*[$P"k9OYTqi&\uu&;l>cr9*U.9=H?!C`R"*ZK7H=&])43M9if%;A56J.!'t;/!`F$A$A!#Ve@$!``Zq-@FL9";R^"2^qEt0!u/3e[bk&^>!,UqL_Zh\+\jmF(d.gWTEe*jM-#gCrQ`(V"DU\.<Qf3M\LkUg+*`X&U$^^/Np&Y=o=C%r)g>+-;&r](b%G;jJq.;ResR^Z76hd2?k8&Yl-fc0--$!bIf*f?t5SDoD1m5W!C0m>DKPmlBAaZUNW=ck,5Zd7q[`@j]MZfB:!`#G*&@G"'sOIfNBN2NZNgSK";N/l=0b]CA]3"pJOC[:cel^adY3Q'(B/+_nW]]DKF)!>?<p9/@\+eP[S'!d4G=dhIsP,J'\4YbcORa.DQk7FDqq"')YW*M8her@[V]+fs_rr_9&,&%~>endstream
endobj
30 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 562
>>
stream
Gau1*?YeCM'ZJu..F)F);GE<+g$W@U/dt@n)Lhe<<Y@9IPUT3l?lsj'kA4XX*X3Q"N4;qMSFa@[JYlno\(q/8#&iBT0TK`S<fdC-,9E;4d(JL7K$[-\;LgGE/"%Vu1,h<2[300++W-n8QQ/;$I@DOb<9`,8>kPrkOeZgZZI)"TM.!`m_+I%.=d<[o\61G]QsH;+=Da&+*L9aF[1@W>@2XIbnT*!DT1l0!.@4u"]V)h67@Fn3f[%tnpS+7a:sjNc/>gSWJBu$T]6+a.d4"mE+9a3nW%&9T($S]XBqB=7#6ImX$0P8qruK(fT#E2VP[3+$E[4VARL!6B6p?S:A#1a!KN9FX"UNFW?KNKElXNtgkhQbRU0kCZZb0fH]]jB6&2\jBYo<Vg-Tg2FK59j'&XmQ:LrTgfl?GGgcj^8')p'u!<@"F>R-Jmeq_e=nc[mE\hB+U9D9]*kQ[>g@lgSX'*qmb/$/YKaZX.d!1i>7'%p2ubm]c3.XA(cmnSa"unK3A('Z?I$C9F*;.V_*1K+ARAUCFeQW"c;EAr5:7QPce'A/s8=M'Ct@~>endstream
endobj
31 0 obj
<<
/Filter [ /ASCII85Decode /FlateDecode ] /Length 1872
>>
stream
Gatm<?$G!^&:N_Cb[\(/W0T!Xp:_i[l)*44,]NH_0`oj4S(]&8kNn8eOhi,S9Tnd_EuJM"\=0t>)U1O`_]N(\:/ZVc3P<,$5T.e45WRdWrrO;*,NAMRUB65f#o3_1BHSMX6a7P@eVAc:+D;;t:uX3:0IRVdhi/0TJ'dS=**M3eLa+Od991687KOKd(hcH&08r5bVf4Q-\V/*(?59fS<gs7d2ps8K,)%aFMqmB*^K'c;V\]]-a2B&RrsnXEc_)-fPl;$'bJ)/H\<08DRG>TSbT6c`"dnB(&cje`je`.D!=?F^MAVG2j'OOrI2XhbWYgP>5oB1p86[R4pGO]Er>=)4"Q>IdoW]j#aSb81f7EP5iQ$aN&,DoLQm!"0Q/eVU*Qb/&:6$QghYSgXN)\QQ/D4YFF0f/@b$s8Mm.SBg^?@+d1SsTOT8%t(;W&/+n0/qrCso53EBcQ(4AWW@No6XO^r58cfLRQ45nm`IEM)f*I%^N]qhJb'pi$e9=(/PSUE(s@j`XKX6oDe;`"c,(!_'tgBV5-ps,>mO3tU1t"r4s[RGRDK.T_rZ@@-5T<XVI"]i<+Vct3gCH951(;.hEC<MR\PA!;uD"Whfcn+?lL>&W2ac:e`%Pd&LbD=B@0(n!KO\LWt$;$=%Z49\lRb+MCqjH$=nK1)r>fPaKu.cbcT'3O^)>%J&b]#])r2'D0B0?s:4:1e+)2X;)M/p*u5ZGM\bPGci:@YNOuKu#%[SYN45D>o2+6^+iR1+b$O,+"/6O(u"V<+^0IT[;d&-I=;ua%mFSHriV%aGhB,HMrg&^KX!EJcB]L6JO40=@)f(F(n'G8YhY^Y98PFM$QIl;NO"S*F:jbG"im#*C\s2r1t*.5,-Zl'rb.2#%[F3aPQ7(rFrqHgn1KsgRltG\G]REq:#f-!Ii\GmM47nEka6$EJqVB/.hqn5h#t-IE`S?NN.+]G-0*5.chf[IHLRT_A);ZX-]C<R-QtWZYPoqg7KsUWH/"<.NGW">h$b)"F0aK-M]=j8nUiuY475$LPQ*%<us0D5=RE7j[I"%p?bu:eFDrJhocYUP=uUj=\Yj_Vu,+U"2r7_id37]+(VprcXj@pe`&R$^t94GKJDEtD]$)b8<2)sK"n58:hF`PY&a^@'!D9=Q9=6W]hFm)?)Ts`]E&*-6c.i]U$n_e_lg=9N%JsPQa,lM!f9:_'Hn=b)A4D79-H7*XDYh=/e)-i:YMo;I?gA@;K)%/X!FZng'b3Cg'-c80H,O/6"nJl@IQY?"ge\!DPn?l+s[a4584QX(JP":^fR)[:?Qq<Ip9@c0A(/Z@oQ</[49f2WM_(`(TiH]0gsE!,SFt5T3QjBg=AC,G+,uciWq[[Z)H3Ee%b/D>l4m=C1!Q"U:4oS]^QGcIG%LGa>,qR0%qf=!qriW7%rbm.>$%'#u%V/`+n+o62J#F3(,`787K?I2f9/nmC7"KnSf1CEq[_S)X4ZC337)1PZbHu3]K:X%<@"r'!RDeCh!oud^Ih7niAt4aVuFq(^I[OXaW2g\f?X#2ob"-K5SS52uJugQ8]VS:NHWb(-8hYeY>^Z=njo#L8]:sM*$Ldj%lJi%R'!rb?ETUEH,<!/^MEEPuap>D2]Oj\PSaT>h,EK([p#sA?/Qb"\#[::U"99_b`3"Oa8"QUIj/tcM#Wq7a:^7)r.p9Nap,k"HXX@\gGfZES&,j-K^b!a5jcXY;NlTFFnIAk_.k`cj@Kn^KI/f+fb`Sc-8VHn&^EL@r!8Vm%=2nLU3Xn5a`W?8A[_UjT#mj']qIl/OFl31p";_KbJUC`A<>XK'',?juE?o%@o=kXD.C?1)Rn6[?ZG;n`\]hmn.4pkHJr\R4978G0T5kI<j3U5%hF$!+GLAJHNc\~>endstream
endobj
xref
0 32
0000000000 65535 f 
0000000061 00000 n 
0000000112 00000 n 
0000000219 00000 n 
0000000331 00000 n 
0000000536 00000 n 
0000000741 00000 n 
0000000856 00000 n 
0000001061 00000 n 
0000001266 00000 n 
0000001471 00000 n 
0000001677 00000 n 
0000001883 00000 n 
0000002089 00000 n 
0000002295 00000 n 
0000002501 00000 n 
0000002707 00000 n 
0000002913 00000 n 
0000002983 00000 n 
0000003287 00000 n 
0000003424 00000 n 
0000005500 00000 n 
0000006623 00000 n 
0000008862 00000 n 
0000011196 00000 n 
0000013948 00000 n 
0000016584 00000 n 
0000019385 00000 n 
0000021802 00000 n 
0000024131 00000 n 
0000026993 00000 n 
0000027646 00000 n 
trailer
<<
/ID 
[<45027f3dfc6bdf37809cbb93991799ac><45027f3dfc6bdf37809cbb93991799ac>]
% ReportLab generated PDF document -- digest (opensource)

/Info 18 0 R
/Root 17 0 R
/Size 32
>>
startxref
29610
%%EOF
ld_Prototype_Guide.pdf…]()


