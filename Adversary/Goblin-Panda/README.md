# Goblin Panda

## Initial Access

Nhóm APT sử dụng một tập tin tài liệu có liên quan tới các chủ đề nổi bật về chính trị quân sự trong nước làm mồi nhử. Các văn bản này khai thác các lỗ hổng liên quan đến RTF (VD: CVE-2017-11882)
Mã khai thác sau đó sẽ drop xuống 3 tập tin: một tập tin thực thi exe có chữ ký hợp pháp của nhà sản xuất phần mềm nhưng chứa lỗ hổng cho phép thực hiện cơ chế DLL Side-Loading, một tập tin dll và một tập tin chứa backdoor đã bị mã hóa.
Mã độc trên máy người dùng sẽ kết nối và gửi dữ liệu tới các máy chủ điều khiển từ xa của nhóm tấn công APT. Lúc này, mọi thông tin nhạy cảm về tài khoản, những dữ liệu mật trên máy người dùng đều có thể bị đánh cắp.

- Goblin Panda using documents targeting to vulnerability in RTF (like CVE-2017-11882)
- The vulnerable documents will download:
  - A legally digital-signed EXE but containing vuln that allow DLL Site-Loading
  - A DLL
  - And a backdoor agent that is obfuscated  
- The malware will then connect to the CnC server of attackers

## Reference
[VCS](https://blog.viettelcybersecurity.com/chien-dich-cua-nhom-apt-goblin-panda-loi-dung-dai-dich-covid-19/)
[Sebdraven](https://sebdraven.medium.com/goblin-panda-changes-the-dropper-and-reused-the-old-infrastructure-a35915f3e37a)
[Fortinet](https://www.fortinet.com/blog/threat-research/cta-security-playbook--goblin-panda)
