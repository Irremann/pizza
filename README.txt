Minetest pizza mod by Irremann

LICENSE: WTFPL

Based and combined ideas from PIZZA MOD jogag's and pizza from camus14

New recipes pizza with two kinds of mushrooms,  with pineapple and chicken, with seafood, with ham and chili pepper.



If caverealms and technic mod installed, then I also recommend adding recipes for the grinder:

if minetest.get_modpath("caverealms") then
    table.insert(recipes, {"caverealms:salt_crystal", "farming:salt 4"})
    table.insert(recipes, {"caverealms:stone_with_salt", "farming:salt 2"})
    table.insert(recipes, {"caverealms:salt_gem", "farming:salt 1"})
end

for _, data in pairs(recipes) do
        technic.register_grinder_recipe({input = {data[1]}, output = data[2]})
end