# Predrag Sterjoski, 213220

2. Slika od Control Flow Graph

  ![labsSlika](https://github.com/predrag17/SI_2023_lab2_213220/assets/109021195/d8a6fc8d-ddc7-47d9-bfce-f30db1c8e9bf)

3. Ciklomatskata kompleksnost e presmetana spored formulata broj na rebra - broj na jazli + 2, taka shto imame 33 broj na rebra, 24 broj na jazli toa e 9 i plus 2 toa e 11.

4. EveryBranch imame 5 test sluchai:
  * user da e null - taka shto kje vleze vo prviot if uslov kje frli iskluchok i kje ide na krajot na funkcijata
  
  * User(null, sterjoskipredrag, soft23#), listata e empty - ovoj test sluchaj kje pokrie taka shto kje vleze vo ifot vo koj se proveruva dali usernameot e null
  posle toa kje si prodolzhi vo delot kade shto se inicijaliziraat stringovite poradi toa shto emailot ne ni sodrzhi nitu @ nitu . . Od tamu kje go proveri ifot vo koj se proveruva dali passwordot e pomal od 8 i dali nekoj karakter se sodrzhi vo username-ot, nema da se ispolni uslovot i kje odi vo else delot kade shto passwordot nema prazno mesto i kje go izvrshi forot kade shto se proveruva dali passwordot ima eden od karakterite na stringot specialCharacters.
  
  * User(predrag17, sterjoskipredrag@gmail.com, soft 23), {(predrag17, sterjoskipredrag@gmail.com, passw1), (softversko, sterjoskipredrag@gmail.com, pass), (predrag17, softversko2023@gmail.com, passwsoft)} - ovoj test sluchaj ni go pokriva forot vo vtoriot if odnosno kade shto se proveruva dali emailot sodrzhi @ ili . , ovoj test sluchaj kje ni gi pokrie site sluchaevi vo toj for, i kje prodolzhi vo kodot pod toj for taka shto kje go ispolni sluchajot kade shto od ifot kade shto se proveruva dali passwordot sodrzhi prazno mesto kje bide ne ispolnet i kje odi vo posledniot return false;.

  * User(predrag, sterjoskipredrag, predrag), empty - ovoj test sluchaj ni go pokriva sluchajot kade shto se proveruva dali nekoj karakter od usernameot se sodrzhi vo passwordot odnosno kje vrati false.
  
  * User(null, sterjoskipredrag, predrag), empty - ovoj test sluchaj ni go pokriva sluchajot kade od if uslovot za proveruvanje dali usernameot e null odnosno negoviot then del kje odi vo ifot pod nego i vo toj if nema da vleze kje odi direktno vo delot pod toj if.
  
 5. Multiple Condition:
 if (user==null || user.getPassword()==null || user.getEmail()==null){
            throw new RuntimeException("Mandatory information missing!");
        }
  * TXX - tuka e lesno odma kje stavime user da e null i kje go proveri samo user == null i kje frli exception.
  * FTX - kje napravime User so (predrag, null, null), emailot ne ni e biten poradi toa shto nas kaj password kje ni vrati T i kje frli iskluchok
  * FFT - (predrag, null, password), tuka emailot go stavame null za da user.getEmail() == null da e True.
  * FFF - User(Predrag, password, email) nema nieden uslov da e tochen i nema da frli iskluchok 
