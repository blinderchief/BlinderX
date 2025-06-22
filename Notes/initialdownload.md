Microsoft Windows [Version 10.0.26100.4349]     
Microsoft Windows [Version 10.0.26100.4349]
(c) Microsoft Corporation. All rights reserved.

E:\coding_challenge_generator>cd backend

E:\coding_challenge_generator\backend>uv init .
Initialized project `backend` at `E:\coding_challenge_generator\backend`    

E:\coding_challenge_generator\backend>uv add fastapi uvicorn sqlalchemy python-dotenv clerk-sdk-python openai
Using CPython 3.13.1 interpreter at: C:\Users\SUYASH KUMAR SINGH\AppData\Local\Programs\Python\Python313\python.exe
Creating virtual environment at: .venv
Resolved 37 packages in 845ms                                               
Prepared 15 packages in 3.67s
░░░░░░░░░░░░░░░░░░░░ [0/35] Installing wheels...                            warning: Failed to hardlink files; falling back to full copy. This may lead to degraded performance.                                                    
         If the cache and target directories are on different filesystems, hardlinking may not be supported.                                            
         If this is intentional, set `export UV_LINK_MODE=copy` or use `--link-mode=copy` to suppress this warning.                                     
Installed 35 packages in 2.02s
 + aiodns==3.5.0                                                            
 + aiohappyeyeballs==2.6.1
 + aiohttp==3.12.13
 + aiosignal==1.3.2
 + anyio==4.9.0
 + attrs==25.3.0
 + brotli==1.1.0
 + certifi==2025.6.15
 + cffi==1.17.1
 + clerk-sdk-python==0.1.0
 + click==8.2.1
 + colorama==0.4.6
 + distro==1.9.0
 + fastapi==0.115.13
 + frozenlist==1.7.0
 + greenlet==3.2.3
 + h11==0.16.0
 + httpcore==1.0.9
 + httpx==0.28.1
 + idna==3.10
 + jiter==0.10.0
 + multidict==6.5.0
 + openai==1.88.0
 + propcache==0.3.2
 + pycares==4.9.0
 + pycparser==2.22
 + pydantic==1.10.22
 + python-dotenv==1.1.0
 + sniffio==1.3.1
 + sqlalchemy==2.0.41
 + starlette==0.46.2
 + tqdm==4.67.1
 + typing-extensions==4.14.0
 + uvicorn==0.34.3
 + yarl==1.20.1

E:\coding_challenge_generator\backend>cd ..

E:\coding_challenge_generator>npm create vite@latest frontend -- --template react

> npx
> create-vite frontend --template react

│
nerator\frontend...
│
└  Done. Now run:

  cd frontend
  npm install
  npm run dev


E:\coding_challenge_generator>cd frontend

E:\coding_challenge_generator\frontend>npm install react-router-dom@6 @clerk/clerk-react

added 211 packages, and audited 212 packages in 25s

33 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities