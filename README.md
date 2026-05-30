# 목차
[참고 링크](#참고-링크) <br />
[Git 사용 가이드(To 자료정리)](#git-사용-가이드to-자료정리) <br />

## 참고 링크
[OpenMRS 데모 사이트](https://demo.openmrs.org) <br />
[보건의료정보학-의료정보시스템.pdf](http://kocw-n.xcache.kinxcdn.com/data/document/2021/dju/byunseunghwan1006/03-1.pdf) <br />
[2024년도 기준 EMR 업체 리스트](https://blog.naver.com/ormchart/223836885794) <br />

## Git 사용 가이드(To 자료정리)

팀 프로젝트(medibridge) 진행을 위한 기본적인 Git 명령어 가이드입니다. 
<br />

### 1. PC 에 원격 저장소와 연결된 폴더가 없을 경우

- [Case A] 원격 저장소에 본인 브랜치가 이미 있는 경우
    ```bash
    # 1. 본인 브랜치로 클론하기
    git clone -b [본인이름] https://github.com/TatTatTaRa/medibridge.git

    # 2. 프로젝트 폴더로 이동
    cd medibridge
    ```

- [Case B] 원격 저장소에 본인 브랜치가 없는 경우
    ```bash
    # 1. 메인 저장소 클론 및 프로젝트 폴더로 이동
    git clone https://github.com/TatTatTaRa/medibridge.git
    cd medibridge

    # 2. 본인 이름의 새 브랜치 생성 및 이동
    git checkout -b [본인이름]

    # 3. 임의로 파일 추가

    # 4. 변경 사항 저장 및 원격 저장소에 브랜치 생성 완료
    git add .
    git commit -m "브랜치 생성"
    git push origin [본인이름]
    ```

### 2. PC 에 원격 저장소와 연결된 폴더가 있을 경우

- [Case A] 원격 저장소에서 파일들을 다운받아야 할 경우
    ```bash
    # 본인 브랜치에서 파일 다운로드
    git pull origin [본인이름]
    ```

- [Case B] 원격 저장소에 파일을 업로드해야 할 경우
    ```bash
    # 1. 현재 폴더의 변경된 모든 파일 등록
    git add .

    # 2. 커밋 메시지 작성 (작업 내용 기록)
    git commit -m "커밋 메시지"

    # 3. 원격 저장소의 본인 브랜치로 업로드
    git push origin [본인이름]
    ```

### 3. 기타

- 브랜치명 변경
    ```bash
    # 1. 로컬 브랜치 이름 변경
    git branch -m [기존브랜치명] [새브랜치명]

    # 2. 새 이름으로 원격 브랜치 업로드
    git push origin [새브랜치명]

    # 3. 기존 원격 브랜치 삭제
    git push origin --delete [기존브랜치명]
    ```
