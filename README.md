# HTML

==실행방법===
Code에서 전체 코드를 복사한 뒤, 해당 코드와 동일한 위치에 Issues에 있는 이미지파일 Programming.png가 위치해 있는 상태에서 .html 파일을 실행하면 Issues에 나와있는대로 실행 결과가 나타납니다.
여기에는 프로그램 코드만 존재하고, Issues에 프로그램 계획서와 사용할 이미지, 프로그램 결과가 나타나 있습니다.

===================================

<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>나만의 컴퓨터공간</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
        }
        #header {
            background-color: #f0f0f0;
            padding: 20px;
            text-align: center;
            font-size: 28px;
            font-weight: bold;
        }
        #container {
            display: flex;
        }
        #menu {
            width: 200px;
            background-color: #e0e0e0;
            padding: 10px;
        }
        #menu button {
            display: block;
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            font-size: 16px;
            cursor: pointer;
        }
        #main {
            flex: 1;
            padding: 20px;
            text-align: center;
            font-size: 18px;
        }
        #footer {
            background-color: #f0f0f0;
            text-align: center;
            padding: 15px;
            font-weight: bold;
        }
        #side-image {
            width: 250px;
            padding: 10px;
        }
        #side-image img {
            width: 100%;
            border-radius: 10px;
        }
    </style>
</head>
<body>

    <div id="header">나만의 컴퓨터공간</div>

    <div id="container">
        <div id="menu">
            <button onclick="showContent('c')">C언어</button>
            <button onclick="showContent('html')">HTML5</button>
            <button onclick="showContent('javascript')">JavaScript</button>
            <button onclick="showContent('python')">Python</button>
        </div>

        <div id="main" id="content">
            중앙 메인 화면<br><br>
            각 언어를 누르면, 각 언어에 대한 설명과 특징이 중앙 화면에 나타남.
        </div>

        <div id="side-image">
            <img src="Programming.png" alt="프로그래밍 이미지">
            <div style="font-size: 14px; text-align: center;">이미지파일<br>Programming.png 사용</div>
        </div>
    </div>

    <div id="footer">컴퓨터공학과 202268023 김해울</div>

    <script>
        function showContent(language) {
            var content = {
                c: `C언어는 1970년대 켄 톰슨과 데니스 리치가 유닉스 운영체제 개발을 위해 개발한 프로그래밍 언어로,
절차 지향적 프로그래밍 방식으로 구현됩니다. C언어는 하드웨어에 직접 접근 가능하고, 메모리를 직접 제어할 수 있는
포인터 기능을 제공하여 효율적인 프로그래밍이 가능합니다.`,
                html: `HTML5는 웹 콘텐츠 구조를 기술하기 위한 마크업 언어 HTML의 최신 버전으로,
웹 개발에 필요한 다양한 새로운 기능과 개선 사항을 제공합니다. 핵심 특징으로는 단순화된 문법, 의미적 요소 강화,
비디오 및 오디오 지원, 오프라인 웹앱 기능, 웹 데이터베이스 기능 등이 있습니다.`,
                javascript: `JavaScript는 객체 기반 스크립트 프로그래밍 언어로, 주로 웹 브라우저에서 웹페이지에
동적 기능을 추가하고 상호 작용을 가능하게 합니다. HTML, CSS와 함께 웹을 구성하는 주요 요소 중 하나이며,
사용자의 행동에 따라 웹페이지를 동적으로 업데이트하고 다양한 인터랙션을 구현하는 데 사용됩니다.`,
                python: `Python은 다양한 분야에서 널리 사용되는 프로그래밍 언어로, 특히 초보자에게 적합한 문법과
가독성이 높은 특징을 가지고 있습니다. 인터프리터 언어로서 빠르게 개발하고 디버깅할 수 있으며,
객체 지향, 절차적, 함수형 프로그래밍 패러다임을 모두 지원합니다.
파이썬은 오픈소스이고 무료이며, 다양한 라이브러리와 프레임워크가 제공되어 개발 생산성을 높여줍니다.`
            };

            document.getElementById("main").innerText = content[language];
        }
    </script>

</body>
</html>
