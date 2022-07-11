<template>
  <main class="container">
    <div class="row">
      <introduction-part/>
      <steps-to-lease-a-car/>
      <personDocumentation :person-documentation="personDocumentation"/>
      <personDocumentation :person-documentation="lawPersonDocumentation"/>
      <i class="fs-5 text-secondary text-start">* НАПОМЕНА: ДОКОЛКУ ПОДАТОЦИТЕ КОИ ГИ ОСТАВАТЕ ПРИ ПРЕД-ОДОБРУВАЊЕТО НЕ СЕ ТОЧНИ И ПРЕЦИЗНИ МОЖНО Е АПЛИКАЦИЈАТА ЗА ЛИЗИНГ ДА ВИ БИДЕ ОДБИЕНА ИЛИ ПРОЛОНГИРАНА
        ОД СТРАНА НА БАНКАТА И ПРИТОА ГО ГУБИТЕ ОСТАВЕНИОТ КАПАР.</i>
    </div>
  </main>
</template>

<script>


import IntroductionPart from "@/components/IntroductionPart";
import StepsToLeaseACar from "@/components/StepsToLeaseACar";
import PersonDocumentation from "@/components/PersonDocumentation";

export default {
  name: 'HomeView',
  data() {
    return {
      lawPersonDocumentation: [
        {
          description: 'Барање за одобрување на лизинг',
          linkName: 'превземи барање',
          goToLink: 'https://s-leasing.mk/content/%D0%91%D0%B0%D1%80%D0%B0%D1%9A%D0%B5%20%D0%B7%D0%B0%20%D0%BE%D0%B4%D0%BE%D0%B1%D1%80%D1%83%D0%B2%D0%B0%D1%9A%D0%B5%20%D0%BD%D0%B0%20%D0%BB%D0%B8%D0%B7%D0%B8%D0%BD%D0%B3_Pravni%20Lica-11.01.2022.pdf'
        },
        {
          description: 'Копија од тековна состојба, не постара од 6 недели',
          linkName: '',
          goToLink: ''
        },
        {
          description: 'Завршна сметка (биланс на состојба и биланс на успех за последните две фискални години)',
          linkName: '',
          goToLink: ''
        },
        {
          description: 'Аналитички заклучни листови кон завршните сметки за последните две години',
          linkName: '',
          goToLink: ''
        },
        {
          description: 'Аналитички заклучен лист за тековната година со последен датум на книжење',
          linkName: '',
          goToLink: ''
        },
        {
          description: 'Согласност за извадок од Македонско Кредитно Биро',
          linkName: 'превземи согласност',
          goToLink: 'https://s-leasing.mk/content/%D0%A1%D0%BE%D0%B3%D0%BB%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%20%D0%B7%D0%B0%20%D0%B8%D0%B7%D0%B2%D0%B0%D0%B4%D0%BE%D0%BA%20%D0%BE%D0%B4%20%D0%9C%D0%B0%D0%BA%D0%B5%D0%B4%D0%BE%D0%BD%D1%81%D0%BA%D0%BE%20%D0%9A%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D0%BE%20%D0%91%D0%B8%D1%80%D0%BE.pdf'
        },
        {
          description: 'Изјава за вистински сопственик',
          linkName: 'превземи согласност',
          goToLink: 'https://s-leasing.mk/content/Izjava-za-vistinski-sopstvenik.pdf'
        }
      ],
      personDocumentation: [
        {
          description: 'ПРОФАКТУРА',
          linkName: '',
          goToLink: ''
        },
        {
          description: 'БАРАЊЕ за одобрување на лизинг',
          linkName: 'превземи барање',
          goToLink: 'https://s-leasing.mk/content/%D0%91%D0%B0%D1%80%D0%B0%D1%9A%D0%B5%20%D0%B7%D0%B0%20%D0%BE%D0%B4%D0%BE%D0%B1%D1%80%D1%83%D0%B2%D0%B0%D1%9A%D0%B5%20%D0%BD%D0%B0%20%D0%BB%D0%B8%D0%B7%D0%B8%D0%BD%D0%B3-Fizicki%20Lica.pdf'
        },
        {
          description: 'Копија од ЛИЧНА КАРТА',
          linkName: '',
          goToLink: ''
        },
        {
          description: 'ПОТВРДА од работодавецот за редовен работен однос',
          linkName: '',
          goToLink: ''
        },
        {
          description: 'Административна забрана од плата од работодавецот',
          linkName: 'превземи Административна забрана',
          goToLink: 'https://s-leasing.mk/content/%D0%90%D0%B4%D0%BC%D0%B8%D0%BD%D0%B8%D1%81%D1%82%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%20%D0%B7%D0%B0%D0%B1%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D0%B4%20%D0%BF%D0%BB%D0%B0%D1%82%D0%B0%20%D0%BE%D0%B4%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BE%D0%B4%D0%B0%D0%B2%D0%B5%D1%86%D0%BE%D1%82%20%D0%B2%D0%BE%20%D0%BA%D0%BE%D1%80%D0%B8%D1%81%D1%82%20%D0%BD%D0%B0%20%D0%A8%D0%9F%D0%90%D0%A0%D0%9A%D0%90%D0%A1%D0%95%20%D0%9B%D0%98%D0%97%D0%98%D0%9D%D0%93%20%D0%94%D0%9E%D0%9E%20%D0%A1%D0%BA%D0%BE%D0%BF%D1%98%D0%B5.pdf'
        },
        {
          description: 'ИЗЈАВА за редовна отплата',
          linkName: 'превземи Изјава',
          goToLink: 'https://s-leasing.mk/content/%D0%98%D0%B7%D1%98%D0%B0%D0%B2%D0%B0%20%D0%B7%D0%B0%20%D1%80%D0%B5%D0%B4%D0%BE%D0%B2%D0%BD%D0%B0%20%D0%BE%D1%82%D0%BF%D0%BB%D0%B0%D1%82%D0%B0.pdf'
        },
        {
          description: 'Годишна даночна пријава (доколку барателот остварува дополнителни приходи)',
          linkName: '',
          goToLink: ''
        },
        {
          description: 'Декларации за прием за бруто плата за последните 3 месеци',
          linkName: '',
          goToLink: ''
        },
        {
          description: 'СОГЛАСНОСТ за извадок од Македонско Кредитно Биро',
          linkName: 'превземи согласност',
          goToLink: 'https://s-leasing.mk/content/%D0%A1%D0%BE%D0%B3%D0%BB%D0%B0%D1%81%D0%BD%D0%BE%D1%81%D1%82%20%D0%B7%D0%B0%20%D0%B8%D0%B7%D0%B2%D0%B0%D0%B4%D0%BE%D0%BA%20%D0%BE%D0%B4%20%D0%9C%D0%B0%D0%BA%D0%B5%D0%B4%D0%BE%D0%BD%D1%81%D0%BA%D0%BE%20%D0%9A%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BD%D0%BE%20%D0%91%D0%B8%D1%80%D0%BE.pdf'
        }
      ]
    }
  },
  components: {
    PersonDocumentation,
    StepsToLeaseACar,
    IntroductionPart
  }
}
</script>
