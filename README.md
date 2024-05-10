# one.piece
if keyboard_check(vk_left)//direita
{
   x-=1
}
if keyboard_check(vk_right)// esquerda
{
   x+=1
}
if place_meeting(x,y+1,obj_wall)//tropeçar para
{
 vspeed = 0
 pulos = 3
}
else
{
 vspeed += 0.3	
}
if keyboard_check_pressed(vk_space) && pulos>0 //pulo sem pulo infinito
{
 vspeed -= 3
 pulos -=1
}
