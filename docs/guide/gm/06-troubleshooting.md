# Troubleshooting

[← GM Guide contents](README.md)

## Player requests are not being processed

- Requests are processed by the active GM's client. When no GM is online, they wait on the player's account and are handled when a GM logs in.
- Sandbox requests are refused while **Players may build sandbox characters** is off, or when the player has reached the per-player limit. The player is told why.
## An option I expect is missing

- Check **GM configuration → Books**. Only the core rulebooks are on by default.
- Check the rarity settings. A tier set to **deny** is hidden everywhere.
- Heritages only list those for the chosen ancestry, plus versatile heritages.

## An option is marked "review" and I cannot create the character

The option's rarity is set to **review**, it has prerequisites Path Keeper cannot check automatically, or it comes from a world or module compendium you have not trusted. A GM can change the rarity setting, trust the compendium under [Trusted compendiums](02-configuration.md#trusted-compendiums), tick **Allow** on the request, or confirm the option and build it by hand on the sheet.

## PF2e still asked me a question during creation

The Review step warned about this choice: it belongs to an item granted several steps removed from anything Path Keeper creates, so it could not be answered in advance. Answer PF2e's prompt as usual. See [PF2e rule choices](../player/03-pf2e-rule-choices.md).

## Some starting equipment was not added

A warning names any item that is no longer in your compendiums or Items directory. Remove it from **Starting equipment**, or restore the item.

## After a system update

If something that used to work now says "could not be read", "not a current option", or "no longer available", check **GM configuration → System compatibility** first: it names the verified version and runs the readers. A compendium re-key in the system (as with the Remaster) can also leave saved plans pointing at items that no longer exist; those plans need their picks made again.

## Upgrading from a private test build

Before its first public release Path Keeper was installed as **Path Keeper (Private Prototype)**, a module with another id. After installing Path Keeper, disable that module in **Manage Modules**, enable **Path Keeper**, and reload. On the first start, Path Keeper copies your configuration, the request queue, approved plans, and every player's plans across by itself, and a notice says when it has. While both modules are enabled nothing is copied and a notice asks you to disable the old one. Uninstall the old module afterwards, from Foundry's Setup screen. Until you do, Foundry's update check reports an error for **Path Keeper (Private Prototype)**: the test builds were never published, so there is nothing to update it from. The error is harmless.

## Known limits

- **Creation:** level-1 characters of every class, including casters: the spellcasting entry (tradition, prepared or spontaneous, attribute, level-1 slots), the chosen starting spells, and the class's own level-1 focus spells come from the installed class features. A spell that only an ancestry's or a feat's text grants, and rituals, may need adding on the sheet; check a new character's Spells tab.
- **What the game system's data does not record:** a few things are listed on Level-up to set by hand, such as a Runesmith's new runes and a Summoner's Eidolon Transcendence at 17.
- **Level-2 test characters:** only classes whose level 2 is a plain class-feat and skill-feat slot.
- **Rule choices:** answered on Review in rounds (an answer's own follow-up choices are asked too) and on Level-up per planned feat; a choice two grants removed from anything the plan creates directly is still asked by the system at creation and is flagged in the request.
- **Not handled:** voluntary flaws (use the sheet's attribute builder), Ancestry Paragon and Dual Class (not modelled by PF2e), and class kits chosen by the player. Free Archetype slots are supported.
- **Organized play preset** does not know about boons or access.
- **Language:** the interface is in English only.
- Verified on Foundry 14.369 with PF2e 8.7.0 and SF2e 1.7.0.

Please report bugs with the repository's issue form, including your Foundry and game system versions. Do not attach exported actors or world data.
