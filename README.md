## Mini-Shakespeare-Chatbot
This project aims to build a bot that will allow the user to converse in modern English and get the corresponding response in ”Shakespearean” or Elizabethan English.

# Let's Talk!
Hey there! So, here's the scoop: I have worked on this really cool project where you can chat away in today's English, and our bot will whisk your words off to Shakespearean times, giving you back that classic Elizabethan flair. How do I do it? Well, I've got a couple of fancy models working behind the scenes. First up, the Dialogue Model. It takes your modern English and crafts a response. Then, we've got the Shakespeare Model, which takes that response and gives it that olde-worlde vibe. I have been testing it out, and folks seem to think it's doing a pretty decent job. Of course, we're still relying on good old-fashioned human judgment for now, seeing as there's not a ready-made stash of modern English-Shakespearean English conversations to measure against. 
Dialog Model : This work try to reproduce the results in [A Neural Conversational Model](http://arxiv.org/abs/1506.05869) (aka the Google chatbot). It use a RNN (seq2seq model) for sentence predictions. It is done using python and TensorFlow.

Shakespeare Model : This part work tries to reproduce the results in [Shakespearizing Modern Language Using Copy-Enriched Sequence-to-Sequence Models](https://arxiv.org/abs/1707.01161). An Attention based pointer copy mechanism is used.


To pretrain the dialog network:

    python main.py --train dialog

To pretrain the Shakespeare  network:

    python main.py --train shakespeare

To test the complete model:

    python main.py --test --dialog_pretrained_model <dialog pretrained model> --shakespeare_pretrained_model <shakespeare pretrained model>

