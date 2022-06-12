<script lang="ts">
    import Drawer, {
        AppContent,
        Content,
        Header,
        Title as DrawerTitle,
        Subtitle,
        Scrim,
    } from '@smui/drawer';
    import TopAppBar, { Row, Section, Title as AppBarTitle } from "@smui/top-app-bar";
    import IconButton from "@smui/icon-button";
    import LayoutGrid, { Cell } from '@smui/layout-grid';
    import Button, { Label } from '@smui/button';
    import List, { Item, Text } from '@smui/list';

    let open = false;
</script>

<TopAppBar dense variant="fixed">
    <LayoutGrid>
        <Cell />
        <Cell>
            <Row>
                <Section>
                    <IconButton class="material-icons" on:click={() => (open = !open)}>menu</IconButton>
                    <AppBarTitle>sample text</AppBarTitle>
                </Section>
            </Row>
        </Cell>
        <Cell />
    </LayoutGrid>
</TopAppBar>
<Drawer variant="modal" bind:open>
    <Header>
        <DrawerTitle>Menu</DrawerTitle>
        <Subtitle>my cool menu</Subtitle>
    </Header>
    <Content>
        <List>
            <Item>test</Item>
        </List>
    </Content>
</Drawer>
<Scrim />
<AppContent>
    <slot />
</AppContent>

<style lang="scss">

</style>