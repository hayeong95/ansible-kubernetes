## Kubernetes 클러스터 관리를 위한 ansible playbook

ansible playbook 실행 방법 (sudo)
```shell
ansible-playbook -u {hostname} -K {path/file.yml}
```

### 개요
* `playlists`: yml 파일 위치 폴더
* `playlists/install-kubernetes`: 쿠버네티스 설치
* `playlists/reset-kubernetes`: 쿠버네티스 초기화

### 사전 작업
* `/etc/ansible/hosts` 파일을 이용하여 서버 그룹 설정

### Kubernetes 설치
1. `install-kubernetes/add-hosts.yml` 수정 후 실행 
2. `install-kubernetes/ready-k8s.yml` 수정 후 실행(1회 재부팅 됨)
3. `install-kubernetes/install-k8s.yml` 수정 후 실행
* 버전 변경 필요 시 `install-k8s.yml` 파일 내 `Install Kubernetes` 부분 수정 (Default: 1.20.15)
