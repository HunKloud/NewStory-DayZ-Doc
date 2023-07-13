# Спавн нового предмета

Зачастую этот список спредметов которые надо создать внутри какого-либо контейнера, однако может быть частью какого либо другого списка

+ __Name__ - Класснейм предмета
    >
    > + Кроме самого класснейма может иметь еще флаги для спавна, все значение идут через символ «|»
    > + На данный момент существуют флаги:
    > + __fillchamber__ - заряжение оружия из внутреннего или внешнего магазина. Данный флаг можно использовать если предмет явялется оружием с внутренним магазинов (SKS, Mosin9130, и др.) или к внешнему магазину [(смотри пример)](https://github.com/HunKloud/NewStory-DayZ-Doc/blob/main/Server/profiles/NewStory/Configurations/RelogBanOnPositions/ItemWithAttachment/demo1.json)
    > + __ammo__ - если мы хотим зарядить опреденным видом боеприпасса то прописывает после флага, через пробел, класснейм патрона [(смотри пример)](https://github.com/HunKloud/NewStory-DayZ-Doc/blob/main/Server/profiles/NewStory/Configurations/RelogBanOnPositions/ItemWithAttachment/demo2.json)
    > + __setinquickbar__ - Если предмет спавнится внутри игрового персанажа и нам нужно поставить его в определенную ячейку быстрого слота, то, через пробел, пишем номер нужной ячейки (номера идут с 1 до 10) [(смотри пример)](https://github.com/HunKloud/NewStory-DayZ-Doc/blob/main/Server/profiles/NewStory/Configurations/RelogBanOnPositions/ItemWithAttachment/demo3.json)
    >
+ __Health01__ - Кол-во хп у предмета от 0 да 1
    >
    > + Список из 1го или 2х элементов.
    > + Если 1 элемент то будет выставлено строго это значение, иначе, будет выбрано случайное значение из этого промежутка.
    >
+ __Quantity__ - Кол-во у предмета (Шкала заполнения или значение стака)
    >
    > + Список из 1го или 2х элементов.
    > + Если 1 элемент то будет выставлено строго это значение, иначе, будет выбрано случайное значение из этого промежутка.
    > + Значения могут принимать как целые числа (далее 1й вариан), так и в промежутке от 0 до 1 (далее 2й вариан).
    > + [Если предмет имеет шкалу заполнения, то 2й вариант.](https://ibb.co/0212X0j)
    > + Если предмет является оружием с внутренним магазинов (SKS, Mosin9130, и др.) или магазином, независимо от наличия шкалы заполения, то 1й вариант.
    >
+ __Inventory__ - Список того, что будет спавниться в инвентаре
    >
    > + Заполняется такими же объектами как и этот
    >

```json
{
    "Hands": {
        "Name": "NSg_Weapon_VAL|SetInQuickBar 1",
        "Inventory": [
            {
                "Name": "NSg_Mag_VAL_30Rnd|Ammo Ammo_9x39AP|FillChamber",
                "Quantity": [30]
            },
            {
                "Name": "NSg_Weapon_VAL_BarrelShort"
            },
            {
                "Name": "NSg_Weapon_Bttstck_Adapter"
            },
            {
                "Name": "NSg_Weapon_M4_Bttstck_GEN3"
            },
            {
                "Name": "NSg_Weapon_GripBox_CQR"
            }
        ]
    },
    "Clothes": [
        {
            "Name": "NSg_Bunny_Hips_Helmet"
        },
        {
            "Name": "NSg_Bunny_Hips_Vest",
            "Inventory": [
                {
                    "Name": "HuntingKnife"
                },
                {
                    "Name": "NSg_Mag_VAL_30Rnd|Ammo Ammo_9x39AP|SetInQuickBar 2",
                    "Quantity": [30]
                },
                {
                    "Name": "NSg_Mag_VAL_30Rnd|Ammo Ammo_9x39AP|SetInQuickBar 3",
                    "Quantity": [30]
                },
                {
                    "Name": "NSg_Mag_VAL_30Rnd|Ammo Ammo_9x39AP",
                    "Quantity": [30]
                },
                {
                    "Name": "NSg_Mag_VAL_30Rnd|Ammo Ammo_9x39AP",
                    "Quantity": [30]
                },
                {
                    "Name": "NSg_Mag_VAL_30Rnd|Ammo Ammo_9x39AP",
                    "Quantity": [30]
                },
                {
                    "Name": "NSg_Mag_VAL_30Rnd|Ammo Ammo_9x39AP",
                    "Quantity": [30]
                }
            ]
        },
        {
            "Name": "NSg_Bunny_Hips_Jacket"
        },
        {
            "Name": "NSg_Bunny_Hips_Pants"
        },
        {
            "Name": "NSg_Bunny_Hips_Boots"
        },
        {
            "Name": "NSg_Bunny_Hips_Belt"
        },
        {
            "Name": "NSg_Bunny_Hips_Backpack",
            "Inventory": [
                {
                    "Name": "WaterBottle|SetInQuickBar 6",
                    "Quantity": [1]
                },
                {
                    "Name": "WaterBottle",
                    "Quantity": [0.5]
                },
                {
                    "Name": "WaterBottle",
                    "Quantity": [1]
                },
                {
                    "Name": "BandageDressing|SetInQuickBar 4",
                    "Quantity": [1, 4]
                },
                {
                    "Name": "BandageDressing|SetInQuickBar 5",
                    "Quantity": [1]
                },
                {
                    "Name": "BandageDressing",
                    "Quantity": [4]
                },
                {
                    "Name": "Lunchmeat|SetInQuickBar 7"
                },
                {
                    "Name": "Lockpick|SetInQuickBar 8"
                }
            ]
        }
    ]
}
```
