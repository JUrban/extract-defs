HOWTO:

1. Take an lm-input that does not have an lm-output yet. E.g. lm-inputs/defsCT/defsCT_325 .

2. Prepend a suitable prompt to it. E.g. prompts/defsCT1 .

3. Run it through your favorite language model (I often use Mistral
Large, but try ChatGPT, Claude, LLama, etc.)

4. If the output is useful, put it under the corresponding name into
the lm-output directory. E.g. lm-outputs/defsCT/defsCT_325-mistral_large .

5. That's it. If you experiment with useful prompts, put them into the
prompts directory. If you have more raw/big inputs, put them
(compressed) into raw-big. Then create a subdirectory in lm-inputs and
split it into small chunks (50 lines seems ok for Mistral Large)
e.g. like this:
```split -l 50 -a 3 -d definitions-CT-all.txt defsCT_```
