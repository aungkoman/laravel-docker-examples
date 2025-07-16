# Using Docker for Laravel

မရှိမဖြစ် မှတ်ထားရမယ့် အခြေခံ Docker Commands တွေ နဲ့ concept တွေ ချရေးထားရမယ်။



```bash
# build and start in detach mode
docker compose -f compose.dev.yaml up -d

# command run ချင်ရင်
# ဒါက container ရဲ့ bash ထဲကို တိုက်ရိုက်ဝင်သွားတာ
docker compose -f compose.dev.yaml exec workspace bash

# ဒါကတော့ bash ကို မဝင်ဘူး တိုက်ရိုက် လှမ်း run တာ
docker compose -f compose.dev.yaml exec workspace php artisan migrate

# ဒါက ရိုးရိုး ဗားရှင်း 
docker compose exec app php artisan migrate
# အပိုင်း ၁ ။​ docker compose exec 
# အပိုင်း ၂ ။​ app 
# အပိုင်း ၃ ။ php artisan migrate

# အပိုင်း ၂ က run ချင်တဲ့ container နာမည်လို့ အကြမ်းဖျဉ်း မှတ်ထားလို့ရမယ်။


# build လုပ်ပြီးသား image ကို ပြန်ခေါ်တာ။

docker compose -f compose.dev.yaml up
```