---
slug: /packager/
hide_table_of_contents: true
---

# TurboWarp Packager

:::info
Use the TurboWarp Packager here: https://packager.turbowarp.org/
:::

The TurboWarp Packager converts Scratch projects into HTML files, zip archives, or executable programs for Windows, macOS, and Linux. It's like HTMLifier and the forkphorus packager.

This is the place where some extra documentation goes. Use the sidebar on the left to navigate.
(async () => {
 
  const response = await fetch('https://yourserver.com/geothermal_questions.json');
  const data = await response.json();
  
  const questions = data.map(item => item.q);
  const answers = data.map(item => item.a);
  
  Scratch.vm.runtime.targets[1].variables["Questions"].value = [];
  Scratch.vm.runtime.targets[1].variables["Answers"].value = [];
  
  questions.forEach(q => {                
    Scratch.vm.runtime.targets[1].variables["Questions"].value.push(q);
  });
  answers.forEach(a => {
    Scratch.vm.runtime.targets[1].variables["Answers"].value.push(a);
  });
})();

const start = Date.now();

const end = Date.now();
const elapsed = Math.round((end - start) / 1000);


Scratch.vm.runtime.targets[1].variables["elapsedTime"].value = elapsed;
(async () => {

  const url = 'https://yourserver.com/geothermal_questions.json';

  try {
    const response = await fetch(url);
    const data = await response.json();

    const questions = data.map(item => item.q);
    const answers = data.map(item => item.a);

    console.log("Questions loaded:", questions);
    console.log("Answers loaded:", answers);

    const runtime = Scratch.vm.runtime;

    runtime.targets.forEach(target => {
      if (target.variables) {

        const questionsListId = Object.keys(target.variables).find(
          key => target.variables[key].name === "Questions"
        );
    
        const answersListId = Object.keys(target.variables).find(
          key => target.variables[key].name === "Answers"
        );

        if (questionsListId && answersListId) {
          
          target.variables[questionsListId].value = [];
          target.variables[answersListId].value = [];

          questions.forEach(q => {
            target.variables[questionsListId].value.push(q);
          });
          answers.forEach(a => {
            target.variables[answersListId].value.push(a);
          });
        }
      }
    });

    console.log("题库加载完成！");
  } catch (error) {
    console.error("加载题库出错:", error);
  }
})();
(async () => {
  const url = 'https://yourserver.com/geothermal_questions.json';
  const runtime = Scratch.vm.runtime;

  function updateLoadingStatus(text) {
    runtime.targets.forEach(target => {
      const loadingStatusId = Object.keys(target.variables).find(
        key => target.variables[key].name === "loadingStatus"
      );
      if (loadingStatusId) {
        target.variables[loadingStatusId].value = text;
      }
    });
  }

  try {
    updateLoadingStatus("加载中... 0%");

    const response = await fetch(url);
    updateLoadingStatus("加载中... 30%");

    const data = await response.json();
    updateLoadingStatus("加载中... 60%");

    const questions = data.map(item => item.q);
    const answers = data.map(item => item.a);

    updateLoadingStatus("加载中... 80%");

      if (target.variables) {
        const questionsListId = Object.keys(target.variables).find(
          key => target.variables[key].name === "Questions"
        );
        const answersListId = Object.keys(target.variables).find(
          key => target.variables[key].name === "Answers"
        );

        if (questionsListId && answersListId) {
function updateLoadingPercent(value) {
  runtime.targets.forEach(target => {
    const loadingPercentId = Object.keys(target.variables).find(
      key => target.variables[key].name === "loadingPercent"
    );
    if (loadingPercentId) {
      target.variables[loadingPercentId].value = value;
    }
  });
}
function updateLoadingPercent(value) {
  runtime.targets.forEach(target => {
    const loadingPercentId = Object.keys(target.variables).find(
      key => target.variables[key].name === "loadingPercent"
    );
    if (loadingPercentId) {
      target.variables[loadingPercentId].value = value;
    }
  });
}
updateLoadingPercent(0);
...
updateLoadingPercent(30);
...
updateLoadingPercent(60);
...
updateLoadingPercent(80);
...
updateLoadingPercent(100);

runtime.startHats('event_whenbroadcastreceived', { BROADCAST_OPTION: 'showMainScene' });

updateLoadingStatus("加载完成！");
runtime.startHats('event_whenbroadcastreceived', { BROADCAST_OPTION: 'startCountdown' });

(async () => {
  const url = 'https://yourserver.com/geothermal_questions.json';
  const runtime = Scratch.vm.runtime;

  function updateVar(varName, value) {
    runtime.targets.forEach(target => {
      const id = Object.keys(target.variables).find(
        key => target.variables[key].name === varName
      );
      if (id) target.variables[id].value = value;
    });
  }

  try {
    updateVar("loadingStatus", "加载中...0%");
    updateVar("loadingPercent", 0);

    const response = await fetch(url);
    updateVar("loadingStatus", "加载中...30%");
    updateVar("loadingPercent", 30);

    const data = await response.json();
    updateVar("loadingStatus", "加载中...60%");
    updateVar("loadingPercent", 60);

    const questions = data.map(item => item.q);
    const answers = data.map(item => item.a);

    updateVar("loadingStatus", "加载中...80%");
    updateVar("loadingPercent", 80);

    runtime.targets.forEach(target => {
      if (target.variables) {
        const questionsId = Object.keys(target.variables).find(
          key => target.variables[key].name === "Questions"
        );
        const answersId = Object.keys(target.variables).find(
          key => target.variables[key].name === "Answers"
        );
        if (questionsId && answersId) {
          target.variables[questionsId].value = [];
          target.variables[answersId].value = [];
          questions.forEach(q => {
            target.variables[questionsId].value.push(q);
          });
