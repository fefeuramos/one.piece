#one.piece
//andar
move = -keyboard_check(vk_left)+keyboard_check(vk_right)

hsp=move*spd

if place_meeting(x+hsp,y,obj_wall)
{
	while !place_meeting(x+sign(hsp),y,obj_wall)
    {
		x+=sign(hsp)
	}
  hsp=0
}

x+=hsp

if place_meeting(x,y+vsp,obj_wall)
{
	while !place_meeting(x,y+sign(vsp),obj_wall)
    {
		y+=sign(vsp)
	}
  vsp=0
}

y+=vsp

if place_meeting(x,y+1,obj_wall)
{
	pulos=1
}
else
{
	vsp+=grav
}
if keyboard_check_pressed(vk_space) && pulos>0	
{
		vsp=jspd
		pulos-=1
}

hsp=0
vsp=0
spd=3
grav=1
jspd=-12
pulos=1
