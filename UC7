
public class OOPSBanApp {

    static class CharacterPatternMap {

        private Character character;
        private String[] pattern;

        // Constructor
        public CharacterPatternMap(Character character, String[] pattern) {
            this.character = character;
            this.pattern = pattern;
        }

        // Getter for character
        public Character getCharacter() {
            return character;
        }

        // Getter for pattern
        public String[] getPattern() {
            return pattern;
        }
    }

    public static CharacterPatternMap[] createCharacterPatternMaps() {

        CharacterPatternMap o = new CharacterPatternMap('O', new String[]{
                " ***  ",
                "*   * ",
                "*   * ",
                "*   * ",
                "*   * ",
                "*   * ",
                " ***  "
        });

        CharacterPatternMap p = new CharacterPatternMap('P', new String[]{
                "***** ",
                "*    *",
                "*    *",
                "***** ",
                "*     ",
                "*     ",
                "*     "
        });

        CharacterPatternMap s = new CharacterPatternMap('S', new String[]{
                " **** ",
                "*     ",
                "*     ",
                " ***  ",
                "    * ",
                "    * ",
                "****  "
        });

        CharacterPatternMap space = new CharacterPatternMap(' ', new String[]{
                "  ",
                "  ",
                "  ",
                "  ",
                "  ",
                "  ",
                "  "
        });

        return new CharacterPatternMap[]{o, p, s, space};
    }

    public static String[] getCharacterPattern(char ch, CharacterPatternMap[] maps) {

        for (CharacterPatternMap map : maps) {
            if (map.getCharacter() == ch) {
                return map.getPattern();
            }
        }

        // If not found, return space pattern
        return getCharacterPattern(' ', maps);
    }

    public static void printMessage(String message, CharacterPatternMap[] maps) {

        for (int row = 0; row < 7; row++) {

            StringBuilder lineBuilder = new StringBuilder();

            for (int i = 0; i < message.length(); i++) {

                char ch = message.charAt(i);
                String[] pattern = getCharacterPattern(ch, maps);

                lineBuilder.append(pattern[row]).append("  ");
            }

            System.out.println(lineBuilder);
        }
    }

    public static void main(String[] args) {

        CharacterPatternMap[] maps = createCharacterPatternMaps();

        String message = "OOPS";

        printMessage(message, maps);
    }
}