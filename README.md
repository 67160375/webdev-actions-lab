# webdev-actions-lab

Lab: GitHub Actions + GitHub Pages

- เว็บไซต์: https://67160375.github.io/webdev-actions-lab/
- ชื่อ: สิทธิวัชร์ อั้นมี
- รหัสนิสิต: 67160375

## Ex.4: Workflow เริ่มเมื่อไร และ job deploy ทำอะไร

Workflow เริ่มทำงานเมื่อมีการ push โค้ดขึ้น branch `main` หรือเมื่อกดสั่งรันเองจากหน้า Actions (`workflow_dispatch`)

ส่วน job `deploy` จะรันบนเครื่อง Ubuntu ของ GitHub โดยทำตามลำดับดังนี้

1. ดึงโค้ดจาก Repository มา (checkout)
2. ตั้งค่า GitHub Pages (configure-pages)
3. แพ็กไฟล์เว็บทั้งโฟลเดอร์เป็น Artifact (upload-pages-artifact)
4. นำ Artifact ไป deploy ขึ้น GitHub Pages (deploy-pages) แล้วได้ URL ของเว็บไซต์ออกมา