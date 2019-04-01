# CnahgeEncoding-task22.task2211
package com.javarush.task.task22.task2211;

package com.javarush.task.task22.task2211;

import java.io.*;
import java.nio.charset.Charset;

/* 
Смена кодировки
*/

public class Solution {

    public static void main(String[] args) throws IOException {

        BufferedReader reader = new BufferedReader(new InputStreamReader(new FileInputStream(args[0]), "Windows-1251"));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(new FileOutputStream(args[1]), Charset.defaultCharset()));

        while (reader.ready()) {
            writer.write(reader.read());
        }

        writer.close();
        reader.close();
    }
}
