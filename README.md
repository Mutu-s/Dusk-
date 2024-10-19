# Dusk-

  > [Discord](https://discord.gg/vCarS52J)


    curl --proto '=https' --tlsv1.2 -sSfL https://github.com/dusk-network/node-installer/releases/download/v0.3.4/node-installer.sh | sudo sh


Daha önce çalıştranlar  import edebilir cüzdanı
    
    rusk-wallet restore

Olmayanlar

    rusk-wallet  
 Create a new wallet SEÇ
 Şifre gir 
 Tekrar gir
 Default Address ENTER
 Moonlight adresimizi kayıt edelim ve Back, Exit

![image](https://github.com/user-attachments/assets/11df5874-a525-4bed-be63-71bfb2c88c1b)

    rusk-wallet export -d /opt/dusk/conf -n consensus.keys
 
 Şifre gir 
 
    sh /opt/dusk/bin/setup_consensus_pwd.sh
 
 Şifre gir 

 Servisi başlat

     service rusk start


 
 Blokları Kontrol edelim Explorer ile

    ruskquery block-height

 > [Explorer](https://apps.dusk.network/explorer/)

SYNC olduktan sonra BOTA !dusk Yazın sonrasında Moonlight adresimizi girin

![image](https://github.com/user-attachments/assets/8c5d5347-2400-4fef-baca-8496c9117b6a)

![image](https://github.com/user-attachments/assets/870b3845-7c24-4896-acfe-80d9f0b8e596)

Bakiye Kontrol

     rusk-wallet moonlight-balance
 
Token geldiyse stake edelim

     rusk-wallet moonlight-stake --amt 1000

![image](https://github.com/user-attachments/assets/7cb5c82d-cd64-4292-a86e-1d3eeddfdfaa)

İşlem tamamlandıktan sonra, aşağıdakileri çalıştırarak staking bilgilerinizi görüntüleyebilirsiniz:

     rusk-wallet stake-info

Düğümünüzün konsensüse katılıp katılmadığını ve blok oluşturup oluşturmadığını görmek için ara sıra şunları kontrol edin:

     grep "execute_state_transition" /var/log/rusk.log | tail -n 5

Bunun biraz zaman alabileceğini unutmayın, çünkü stake'inizin olgunlaşması için en az 2 dönem veya 4320 blok gerekir. Toplam stake'inize göre stake'iniz de bir faktördür.

Her şey yolunda giderse ve düğümünüz blokları kabul etmeye ve oluşturmaya başlarsa, Nocturne düğümünüzü başarıyla kurmuşsunuz demektir!


