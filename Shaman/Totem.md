Target Windfury Totem, if in duel range (9.9 yards) target last target, else cast Windfury Totem (edit III and YOURNAME)

/run TargetByName("Windfury Totem III YOURNAME", exactMatch) if not CheckInteractDistance("target",3) then CastSpellByName("Windfury Totem")else TargetLastTarget()end



Cast Frost Shock, else Earthbind totem

/cast Frost Shock
/run TargetByName("Earthbind Totem YOURNAME", exactMatch) if not CheckInteractDistance("target",3) then CastSpellByName("Earthbind Totem")else TargetLastTarget()end

 

Mana Tide Totem, Healing Wave(Rank 4)

/run if UnitMana("player")< 1000 then CastSpellByName("Mana Tide Totem")CastSpellByName("Healing Wave(Rank 4)") else CastSpellByName("Healing Wave(Rank 4)")end

 

Re-popping totems using the cheapest rank 1 spells. (Clicking faster than the global cooldown will skip totems)

/run s={"Fire Resistance Totem(Rank 1)","Nature Resistance Totem(Rank 1)","Stoneskin Totem(Rank 1)","Frost Resistance Totem(Rank 1)"} if q==nil then q=0 end q=q+1 if q>getn(s) then q=1 end CastSpellByName(s[q])

 

Castsequence Windfury, Strenght of Earth, Mana Spring

/run local _gspells = { "Windfury Totem", "Strength of Earth Totem", "Mana Spring Totem"} if GetSpellCooldown(4,"BOOKTYPE_SPELL")==0 then _gi=_gi and _gi > 0 and _gi or 1 CastSpellByName(_gspells[_gi]) _gi = math.mod(1+_gi, 1+table.getn(_gspells))end

 

Windfury, Strenght of Earth, Mana Spring

/run s={"Windfury Totem","Strength of Earth Totem","Mana Spring Totem"} if q==nil then q=0 end q=q+1 if q>getn(s) then q=1 end CastSpellByName(s[q])

 

Start attack, Searing Totem

/run for z=1,172 do if IsAttackAction(z)then if not IsCurrentAction(z)then UseAction(z);end;end;end;
/cast Searing Totem

 

Low rank Magma Totem, max rank if combat

/run if not UnitAffectingCombat("player") then CastSpellByName("Magma Totem(Rank 1)") else CastSpellByName("Magma Totem") end



This macro allows for a second totem to be attached to the same key, while ALT is being hold down aswell.

/script if (IsAltKeyDown())then CastSpellByName("TOTEM NAME FOR SHIFT+ALT") else CastSpellByName("TOTEM NAME FOR SHIFT") end



If you got Windfury on mainhand cast Grace of Air Totem, else Windfury Totem

/run hasMainHandEnchant = GetWeaponEnchantInfo() if  not hasMainHandEnchant then CastSpellByName("Windfury Totem")else CastSpellByName("Grace of Air Totem")end

 

If you got Windfury on mainhand cast Tranquil Air Totem, else Windfury Totem

/run hasMainHandEnchant = GetWeaponEnchantInfo() if  not hasMainHandEnchant then CastSpellByName("Windfury Totem")else CastSpellByName("Tranquil Air Totem")end

 

If you got Windfury on mainhand cast Grounding Totem, else Windfury Totem

/run hasMainHandEnchant = GetWeaponEnchantInfo() if  not hasMainHandEnchant then CastSpellByName("Windfury Totem")else CastSpellByName("Grounding Totem")end