기가지니 시스템 분석
==================

## 기가지니 서비스 개요
1. [GiGA Genie Voice Kit](https://gigagenie.ai/resources/voiceKit)
  - [wiki](https://github.com/GiGAGenie-VoiceKit/UserGuide/wiki)
  - 음성 인식 서비스
  - 개발자들이 필요한 음성을 등록하기 위한 서비스로 실제 서비스 하는데 필요한 서비스라기보다는 서비스를 만들기 위한 서비스
  - 필요 기술 : 없음
  - 비트코인, 이더리움 등 일상에서는 사용하지 않았을 단어들을 등록 할 수 있습니다.
  - 정확하게는 단어 자체를 등록하기 보다는 음성인식이 잘 안될 때 보정하는 데이터 등록으로 보여 집니다.

2. [GiGA Genie Dialog Kit](https://gigagenie.ai/resources/dialogKit)
  - [wiki](https://github.com/gigagenieDmt/DialogKit-deploymentGuide/wiki)
  - 자연어 처리 서비스
  - 위에 등록된 음성과 기가지니에 기 등록된 음성을 파악하여 서버(3rd party)에 데이터를 전송할 수 있는 서비스
  - 이 서비스를 통해서 비트코인등과 같은 코인을 사거나 지금 시세를 화면 출력과 같은 일을 할 수 있습니다.
  - 음성을 분석하고 데이터를 만드는 일은 기술이 필요하지 않습니다. https://github.com/gigagenieDmt/DialogKit-deploymentGuide/wiki/3.-대화모델-관리(DMT)-메뉴-이해하기
  - 위에서 등록되어 분석된 데이터를 서버에게 보내고 어떠한 행위를 위해서는 서비스 로직을 등록하여야 합니다.
  - 서비스 로직은 nodejs, python 으로만 등록 가능합니다. https://github.com/gigagenieDmt/DialogKit-deploymentGuide/wiki/5.-서비스로직-관리하기-(선택)
  - 서비스 로직을 통해서 정확하게 어떠한 행위를 할 수 있는지는 파악하기 힘듭니다.

3. [GiGA Genie Home IoT API](https://gigagenie.ai/resources/homeiotapi)
  - IoT 서비스

4. [GiGA Genie Multilingual API](https://gigagenie.ai/resources/multilingualapi)
  - 다중언어 서비스로 번역 & 통번역 서비스

5. [GiGA Genie TTS API](https://gigagenie.ai/resources/ttsapi)
  - 음성합성 서비스
  - TTS API 를 이용하여 지금 시세를 화면에 출력하는 것이 아니라 음성으로 안내 할 수 있습니다. ex) 지금 비트코인의 시세는 (얼마)입니다.
  - 아직 API가 공개 되지는 않았습니다.

6. [GiGA Genie Vision API](https://gigagenie.ai/resources/visionapi)
  - 영상 AI 서비스

7. [GiGA Genie Service SDK](https://gigagenie.ai/resources/serviceSdk)
  - [wiki](https://github.com/GiGAGenie-ServiceSDK/UserGuide/wiki)
  - GiGA Genie App SDK
  - 위의 모든 행위들을 GiGA Genie App 형태로 지원
  - 음성인식부터 Dialog TTS 까지 APP 네에서 처리하는 방식

## 결론
  - 서비스의 형태에 따라서 달라질 수 있지만 기본적으로 Dialog Kit을 이용하여 간단한 질의 응답 서비스는 가능해 보입니다.
  - 다양한 서비스와 TV UI를 통한 화면 처리 등을 하려면 SDK를 이용하여 앱을 개발해야 하는 것으로 파악됩니다.