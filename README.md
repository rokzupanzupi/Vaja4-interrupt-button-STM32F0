b) Glede na vašo razvojno ploščico in razširitveno vezje s tipkami, izberite ustrezen digitalni vhod kot interrupt (GPIO_EXT…) in izhod za zeleno LED. Zapišite izbrana pina:
Odgovor: GPIO_EXTI0 -> PA0 ter zelena led PC9 in modra led PC8.


d) Znotraj te funkcije zapišite ukaz za vklop/izklop zelene LED (pomagajte si z metodo toggle, glej vaja0a).
Odgovor: HAL_GPIO_TogglePin(GPIOC,GPIO_PIN_9).

e) Znotraj iste funkcije dodajte še zakasnitev, ki je potrebna, ko uporabimo mehanska tipkala/stikala: for(uint32_t i=0; i<10000; i++); Koliko znaša (v mili sekundah) zapisana zakasnitev?
Odgovor: 500ms.

f) V user code begin 3 - zanka while(1) - zapišite ukaz za utripanje modre LED (metoda toggle, glej vaja0a):
Odgovor: HAL_GPIO_TogglePin(GPIOC,GPIO_PIN8);.

g) V to zanko dodajte ukaz za zakasnitev z funkcijo Delay iz knjižnice HAL, in sicer pol sekunde (glej vaja0a):
Odgovor: HAL_Delay(500).

b) Opazujte delovanje (utripanje modre LED). Kaj se zgodi, ko pritisnemo na modro tipko na STM32F0?
Odgovor: Ko pritisnemo modro tipko se prižge ali ugasne zelena LED in ostane v tem stanju, modra LED ves čas utripa.

c) Ali pritisk na modro tipko vpliva na utripanje modre LED in zakaj?
Odgovor: Ne, ker pogram poteka, pritisk na tipko pa je samo interupt za zeleno LED luč. Napisan pa je tudi v drugem USER CODE BEGIN.

Komentar: Z vajo nisva imela težav.
