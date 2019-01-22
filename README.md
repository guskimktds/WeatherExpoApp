# WeatherExpoApp

제목 : React native 날씨앱 Expo 버전

목적 : 날씨앱을 Expo client 방식으로 만들었다

기반기술 : React Native 0.57, Expo, NPM, Node.js

아키텍처구성 : 로컬PC(노트북)에 EXPO 환경에서 빌드 -> 단말에서 EXPO client app 을 설치 QR 코드를 읽으면 expo (NPM)에서 서비스 처리
외부연동( api.openweathermap.org ) api 호출하여 current 날씨정보를 json 형식으로 가져옴

component UI 는 아래와 같이 flexbox 와 LinearGradient, MaterialCommunityIcons 를 임포트 받아서 처리

import {LinearGradient} from "expo";
import { MaterialCommunityIcons } from "@expo/vector-icons";

<--flex box 처리방식 start -->
const styles = StyleSheet.create ({
  container: {
    flex: 1
  },
...

<--flex box 처리방식 end-->

api 호출 시 key를 미리 생성해야함(10분 후 연동 가능)
