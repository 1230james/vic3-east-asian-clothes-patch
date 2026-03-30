# 01_clothes.txt is identical to vanilla.
# 01_headgear.txt is identical to vanilla.
# 
# 01_hairstyles.txt is MOSTLY identical to vanilla, but adds the following trigger logic:
# 
# AND = { # EAC/EACP - Extend Buddhist non-hair to leaders of Buddhist theocracies
#     exists = scope:character
#     scope:character = {
#         religion = {
#             has_discrimination_trait = buddhist
#         }
#         is_ruler = yes
#         owner = {
#             has_law = law_type:law_theocracy
#             ig:ig_devout = {
#                 NOT = {
#                     has_ideology = ideology:ideology_confucian
#                 }
#             }
#         }
#     }
# }
# 
# as a case in the big OR block for `buddhist_monk_non_hair`.