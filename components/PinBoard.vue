<template>
  <div class="pinboard-container">
    <div class="pinboard">
      <div class="ratio"></div>
      <div class="content-wrapper">
        <div class="content">
          <HorizontalSticky>Eieren halen</HorizontalSticky>
          <HorizontalSticky>Campagne idee: big floppa</HorizontalSticky>
          <HorizontalSticky>wachtwoord: M@rkrutte123!</HorizontalSticky>
          <HorizontalSticky>Geen domme dingen doen</HorizontalSticky>
          <HorizontalSticky>Aan geheugen werken</HorizontalSticky>
          <HorizontalSticky>Lekken naar de pers</HorizontalSticky>
          <LargeSticky>
            Ervoor zorgen dat in ieder geval vera bergkamp mij mag
          </LargeSticky>
          <LargeSticky>
            <ul>
              <li>Hallo</li>
              <li>Hallo</li>
              <li>Hallo</li>
              <li>Hallo</li>
            </ul>
          </LargeSticky>
          <LargeSticky>
            Zorgen dat Wilders & Baudet niks zeggen over de motie van wantrouwen
            tegen mij in de toekomst
          </LargeSticky>
          <LargeSticky>
            TODO:
            <ul>
              <li>
                Coronamaatregels versoepelen zodat het volk mij weer leuk vind
              </li>
            </ul>
          </LargeSticky>
          <LargeSticky>
            Idee: "anonieme bron" noemen als reden dat ik het me herinner
          </LargeSticky>
          <LargeSticky>
            Wraak nemen op Clash of Clans dorp van Hugo
          </LargeSticky>
          <LargeSticky>
            Niet vergeten elke dag op farmville in te loggen zodat ik mijn
            muntjes niet kwijt raak
          </LargeSticky>
          <LargeSticky>
            <b>Niet vergeten</b>: de zogenaamde "default dance" leren zodat ik
            stemmen krijg van jongeren
          </LargeSticky>
          <LargeSticky>
            <img
              src="https://media1.giphy.com/media/L0f1Mj7SPaq9pO93By/200.gif"
              style="width: 100%; height: 150px"
            />
          </LargeSticky>
          <LargeSticky>
            <div class="move-form-here">
              <script>
                document
                  .querySelector('.move-form-here')
                  .appendChild(document.querySelector('.is-netlify'))
                document
                  .querySelectorAll('.is-netlify[hidden]')
                  .forEach((el) => el.removeAttribute('hidden'))
              </script>
            </div>
          </LargeSticky>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.pinboard-container {
  background: url(http://2.bp.blogspot.com/-HPWq5_H10Bs/U4NbaH3_WoI/AAAAAAAAO-w/3tOklJ2MBcE/w1200-h630-p-k-no-nu/Seamless_Natural_Wood_Texture.jpg);
  padding: 10px;
  user-select: none;
}
.pinboard {
  width: 100%;
  background: url(https://st.depositphotos.com/1032753/4936/i/950/depositphotos_49366379-stock-photo-seamless-pinboard-texture.jpg);
  position: relative;
  overflow: hidden;

  .ratio {
    height: 80vh;
  }
  .content-wrapper {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;

    .content {
      position: relative;
    }
  }
}
</style>
